# The CAP/PACELC theorems and blockchains
The [CAP Theorem](https://en.wikipedia.org/wiki/CAP_theorem) relates to a fundamental property of a distributed system, it can have two of the following three read/write pair properties:
1. Consistency (*C*): A client request returns the most recent write, i.e., all clients have the same view of the data at any given time.
2. Availability (*A*): A functioning node will not return an error or timeout, i.e., each client always receives a response following a read or write request.
3. Partition tolerance (*P*): The system continues to function when parts of the network become physically disconnected due to failure.

In essence, a network of interconnected nodes that share data always run the risk of network failures and consequently network partitioning. Since a distributed system by definition must be partition tolerant, the choice is really between *C* and *A* when a network failure occurs.

When a network is partitioned, a client request to a node either returns an error or a time-out (if *C* is chosen over *A*), or its most recent data state at the risk of inconsistent data across the network (if *A* is chosen over *C*).

<span style="color:red">CAP is best illustrated. Some rules for the illustration:
<br>C+P is good for business needs when there can be no flexibility around when the data between nodes synchronizes.
<br>C+A is good for business needs where there can be flexibility around when the data between nodes synchronizes.</span>

When the network is operating without network partitions, both consistency and availability are possible. However, under such normal operations there is another tradeoff between latency (*L*) and *C*. This tradeoff lies at the core of the [PACELC theorem](http://cs-www.cs.yale.edu/homes/dna/papers/abadi-pacelc.pdf).

Additionally, PACELC describes one of the more fundamental insights within blockchain designs: the block generation rate and [the need to reward miners/validators](https://medium.facilelogin.com/the-mystery-behind-block-time-63351e35603a) for [honest orphan blocks](https://www.blockchain.com/btc/orphaned-blocks) if a node receives multiple valid blocks. [Decker and Wattenhofer (2013)](https://www.tik.ee.ethz.ch/file/49318d3f56c1d525aabf7fda78b23fc0/P2P2013_041.pdf) showed that a new Bitcoin block propagates to 95% of the nodes within 12.6 seconds. This is more than enough time for a miner to work on solving a block, and broadcasts a successful solution, before it hears about a change in the block height. In fact, we should expect it to happen \(12.6\600 \approx 2.1%\) in Bitcoin. Today, this number is far lower. The main reason for this is the Bitcoin relay network, which drastically [reduces latency for block propagation](http://bitcoinrelaynetwork.org/stats.html). Today, using that relay network, 95% of the nodes receive block information within 616 milliseconds.

## Do blockchains violate CAP/PACELC?
Short answer, no it does not violate the two theorems. Blockchains achieve fault tolerance using state replication&mdash;blocks propagate throughout the network and all full nodes share a history. Consistency is secured using a consensus model, e.g., chain with most work + PoW in the Nakamoto design. Availability is high as it is enough for a new node to connect to a single other node in the network and ask that node for a list of peers.

However, depending on the <span style="color:red">consensus model</span>, consistency and availability differs. Some designs, e.g., the Nakamoto design, relies on eventual consistency. That is to say, the Nakamoto design is a \(P+A\) system where there is a temporal lag between \(P+A \text{and} C\). Here, consistency is not immediate, but rather achieved over time through validation and new blocks being appended to the blockchain. Other designs, for instance those that rely on practical Byzantine Fault Tolerance (e.g., Tendermint), can favor \(P+C\) systems.

To understand why certain systems would favor one or the other, we must examine the concept of finality.

## Finality
Finality an inherent characteristic of all blockchain systems. Finality is the possibility of a validated block to be revoked after it has been successfully appended to its blockchain. Three different types of finality exist:
1. **Immediate finality**: pBFT based systems (e.g., Tendermint) guarantee transaction finality the same moment the block is added to a blockchain. Many elective consensus models can guarantee absolute finality due to the way node roles (e.g., leaders and validators) work together in a trusted setting.
2. **Probabilistic finality**: Here, the likelihood of an appended block being revoked decreases with each new block appended to the chain. The reason for this can vary between consensus models. The one most suitable for probabilistic finality is arguably PoW. Here, the likelihood increases due to the fact that it is increasingly unlikely that another chain with more work (and thus expended energy) will replace the one containing our block.
3. **Stake based finality**: Here, revoking a block is discouragingly costly for the validator. Consensus models relying on PoS (or a hybrid of PoW+PoS) are particularly suitable for stake based finality. Here, if a validator uses their stake on two conflicting chains&mdash;thus threatening consistency&mdash;that validator risks harsh punitive actions. Vitalik Buterin wrote a [great blog post in 2014](https://blog.ethereum.org/2014/01/15/slasher-a-punitive-proof-of-stake-algorithm/) laying the foundations for how such a mechanism could be designed. Since then, must has happened and work is still ongoing (read more [here](https://medium.com/@VitalikButerin/minimal-slashing-conditions-20f0b500fc6c) and [here](https://arxiv.org/pdf/1710.09437.pdf)).

Finality becomes an important consideration in combination with the CAP and PACELC tradeoffs. Consistency favoring systems would not allow transaction requests to go through in the event of a network partition. By contrast, availability favoring systems would allow transactions to go through under the same conditions. In her [Medium article on the subject](https://medium.com/mechanism-labs/finality-in-blockchain-consensus-d1f83c120a9a), Alexis Gauba succinctly describe up the relationship between finality and CAP as follows:
> Consistency favoring systems provide BFT finality, while availability favoring systems provide probabilistic finality.

That same Medium article also describes the problem with blockchains that support both payments (an application where \(P+A\) with eventual \(C\) is sufficient) and decentralized Applications (dApps) that utilize smart contracts. Alexis correctly points out that certain dApps will favor availability (e.g., supply chain event logs where immediate finality is not necessary), whereas others require consistency (e.g., a transactive system for real time trading of electricity where immediate finality is required).

## Synthesis and concluding remarks
Different business applications will find certain blockchain designs more or less favorable. It is therefore of crucial importance to understand how different platforms and blockchain designs relate to CAP/PACELC and finality.

<span style="color:red"> LIST BUSINESS APPLICATIONS AND SUITABLE CAP/PACELC + finality tradeoffs. ALSO CHECK [ALEXIS ET AL 2018 FOR MORE INFO](https://github.com/Mechanism-Labs/MetaAnalysis-of-Alternative-Consensus-Protocols/blob/master/MetaAnalysis.pdf) and the blog post [here](https://medium.com/mechanism-labs/finality-in-blockchain-consensus-d1f83c120a9a)</span>

Consensus model table (adopted from [ALEXIS ET AL 2018 FOR MORE INFO](https://github.com/Mechanism-Labs/MetaAnalysis-of-Alternative-Consensus-Protocols/blob/master/MetaAnalysis.pdf)). <span style="color:red">But this table seems weird given the block quote above. Check later</span>.

| Consensus model | CAP | Finality |
|-------------------|-----|---------------|
| Tendermint | PC | Immediate |
| Thunderella | PA | Probabilistic |
| Algorand | PC | Probabilistic |
| Dfinity | PC | Probabilistic |
| Ouroboros Genesis | N/A | Probabilistic |
| Casper FFG | PC | Stake based |
| Casper TFG | PA | Probabilistic |
