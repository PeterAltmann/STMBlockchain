# Blockchain defined
## Definitions and key concepts
**Simple definition**

>A technology that enables a distributed network of actors to reach consensus around a shared data state *without the need* of a central coordinating authority.

**Technical definition**

> An amalgamation of technologies that together enable a cryptographically secured append-only immutable ledger that is shared and updated across a distributed network of actors *without the need* of a central coordinating authority or any third party actors.

Now, let us look at these keywords in detail.

**Distributed network**: A distributed network means that there is no central communication point in the network. Instead, all network actors communicate directly with each other in a [peer-to-peer fashion](https://en.wikipedia.org/wiki/Peer-to-peer).  Note, however, that distributed systems still rely on a central authority to govern the entire system. Compratively, decentralized systems do not. However, not all blockchain designs are decentralized. Consequently, both definitions highlight *without the need* to reflect the reality that some blockchains rely on centralized authorities and are thus not necessarily decentralized.

**Amalgation of technologies**: Blockchain technology is not a new technology, but rather a novel combination of existing technologies. These include: distributed networks, [symmetric and asymmetric encryption](https://en.wikipedia.org/wiki/Cryptography#Modern_cryptography), [Merkle trees](https://en.wikipedia.org/wiki/Merkle_tree), [economic countermeasures for denial of service attacks and spam](https://en.wikipedia.org/wiki/Proof-of-work_system), [hash-linked immutable data states](https://patents.google.com/patent/US5136646A/en), [cryptographic hash functions](https://en.wikipedia.org/wiki/Cryptographic_hash_function), [consensus](https://en.wikipedia.org/wiki/Consensus_(computer_science), [distributed state replication](https://en.wikipedia.org/wiki/State_machine_replication), and [economic incentive alignment](https://en.wikipedia.org/wiki/Mechanism_design).

**Cryptography**: Blockchains rely extensively on cryptography for its security features (e.g., immutable history), for its identity system, and its various operations and features (e.g., creating transactions and mining to secure the past state and validate appended blocks). <span style="color:red"> The extensive use of cryptography warrants its own chapter.</span>

**Append only**: The past state of data in a blockchain is immutable. Data can thus not be changed, only added, i.e., appended in a sequential way where each block links to previous blocks using [hash links](https://patents.google.com/patent/US5136646A/en).

**Shared and updated**: Blockchains utilize various consensus models and consenus algorithms to reach agreement around a given data state across a distributed network (<span style="color:red">more here</span>). Rather than relying on a coordinating actor, blockchains can (not must) use a protocol for what constitutes a valid addition and how these additions are propagated throughout the network. These protocols differ in various ways depending on intended use case (<span style="color:red">more here</span>).

## Glossary and common keywords
[Andreas Antonopoulos has a great glossary that can be found here](https://github.com/bitcoinbook/bitcoinbook/blob/develop/glossary.asciidoc). However, some additional concepts worth mentioning are as follows.

**Block header**: Contains metadata for each block (<span style="color:red">described in detail below under A Nakamoto block</span>).

**Candidate block**: Miners create candidate blocks with transactions from a memory pool. They then attempt to mine the candidate block. If mined, the candidate block is appended to the blockchain.

**Node**: Nodes are network actors who carry out a number of different functions. First, they maintain a copy of the blockchain. Second, nodes either create and broadcast transactions or listen for broadcasted transactions, propagate these transactions, and ensure that the transactions follow consensus rules. Third, nodes keep valid transactions in something called a memory pool from which miners select transactions to include in a block. Fourth, nodes listen also to confirmed transactions. When a miner (a certain type of node) finds a correct nonce, it broadcasts the confirmed block to the network, and nodes append this block to their local copies. Some blockchain designs allow for additional node functionality, e.g., lightweight nodes that verify payments, masternodes that offer additional services (e.g., anonymity and instant transactions), and voting rights for governance.

**Permissioned blockchains**: Also called *private* (completely centralized) or *consortium* (open to a consortium of industry actors) blockchains. These blockchains restrict data access rights to a validated list of participants. Commonly deployed by  industry consortia and high performance blockchains (<span style="color:red">read more here</span>).

**Permissionless blockchains**: Also called *open* blockchains. These blockchains have no restrictions on participation and anyone who follows the protocol rules can take part in securing the past state and proposing state changes. (<span style="color:red">read more here</span>).

**Private key**: A 256 bit random number used for the generation of the public key. It is used to authenticate any transaction you wish to make.

**Public key**: Generated from the private key. It is analogous to an account number that you can use for transactions.

**Smart contract**: Smart contracts are computer programs that run on top of certain blockchains. Smart contracts, regardless of what their name might suggest, are not like legal contracts in a traditional sense. Rather, they are more akin to rule sets that execute when certain conditions are met.<span style="color:red"> More here.</span>

**State machine**: Network actors modify a blockchain's given state as a result of transactions, validation of transactions, and the final propagation of appended blocks. In essence, blockchains are systems where actors reach consensus around valid state changes in a decentralized way ([read more here](https://blog.markshead.com/869/state-machines-computer-science/)).

**Target difficulty**: The target threshold for the block header hash digest. Decides how difficult it is to mine a block.

**Turing complete blockchains**: The Nakamoto blockchain design is intentionally not Turing complete. Rather, it uses a limited language that is designed to allow only essential operations that enable the transfer of tokens from one address to another address. By contrast, a Turing complete blockchain allows for arbitrary programs and can perform any computation.

**Virtual machine**: Some Turing complete blockchains run virtual machines that allow code&mdash;in the form of smart contracts&mdash;to be run on a blockchain.<span style="color:red"> More here.</span>

## The blockchain technology stack
To understand how blockchain technology works, and how it can be monetized, it is helpful to explore the blockchain technology stack. Each part will be described (with the exception of the base [Internet layers](https://en.wikipedia.org/wiki/Internet_protocol_suite)), together with a discussion around its value creation and capture potential. <span style="color:red"> perhaps even with some links to projects, but that can be done later once I tie it all together with the use cases part etc.</span>

<span style="color:red">this should be an imagine later</span>**The technology stack and its value creating potential.**

| Layer | Contains | Details | Value logic (speculative examples)|
|-----------------------|------------------------------|-----------------------------------------------------------|----------|
| Infrastructure | Validators, nodes, and users | The various actors in the blockchain network. | Supply mining services and hardware. |
| Blockchain protocol | Consensus model | The way the network agrees on a particular data state. | N/A |
|  | Data state changes | The rules for how the data state is updated. | N/A |
|  | Participation | Permissionless (open) or permissioned (closed). | Charge for access. |
|  | Virtual machine | A DoS protected runtime environment for smart contracts. | Tokenized code execution cost. |
| Overlay network | Smart contracts | A rule set with conditional execution. | Contract execution fees. Contract development services. |
|  | Digital data feeds | Mechanism for actors to receive updated digital data. | Unknown |
|  | Oracles | Cyber-physical data feed links. | Charge for access to cleaned and curated data. |
|  | Off-chain computing | Verifiable off-chain computations using oracles. | Data analytics. |
|  | Governance | Ways decisions are made (off-chain and on-chain). | Unknown |
|  | State channels | Two-way communication path between two actors. | State channel service fees. |
|  | Side chains | A separate blockchain that is pegged to a main chain. | Development services. |
|  | Data storage | A distributed method of storing and sharing data. | Storage fees. |
| Decentralized Economy | Digital identity | An actor's identification and authorization mechanism. | Unknown |
|  | Asset mapping and tracking | Digital representations of physical and digital assets. | Cost efficient operations. |
|  | Reputation | Logs of past behavior that vouch for future behavior. | Lowers costs for economic activity. |
| Application | Decentralized Applications | An application run on a decentralized trustless protocol. | Development services. Fees. Marketing. |
|  | dApps browser | An access point for decentralized applications. | Fees. Curated lists. Marketing. |
| UXI | Wallets | An access point for blockchain tokens. | Fees. Marketing. |

<span style="color:red">Value network effects (tokens worth more if used, fat protocols. that marketing side thingy)
mining
MaaS
how to monetize each?</span>

## A Nakamoto block
Now we look examine the ledger itself. One key concept is the *block* itself. A block contains data fields and represents a structure that organizes the ledger.

**A Nakamoto block.** Each cell represents 1 byte of data (total in parenthesis).
![](images/blockstructure.png)

Note that the specifics related to the data fields vary between different blockchain designs.

- **Magic_Number**: A 4 bytes long identifier for the network. Each blockchain network has its own unique identifier. It is used to segment data in a continuous data stream (every message starts with the Magic Number).
- **Block_Size**: This field indicates how large the block is.
**Version**: Details the block validation rules that the block follows. This number lets everyone know what rules were applied when the block was created. When the [rules change](https://bitcoin.org/en/version-history), the block version number may change too.
- **Hash_Previous_Block**: This data field is generated by twice hashing the block header of the previous block to which this block was appended.
- **Hash_Merkle_Root**: Derived from all the transactions (i.e., recorded events such as transactions) included in the block. Since each transaction is part of this hash digest, it is impossible to alter a transaction without changing this data field.
- **Time**: The number of seconds that has transpired since January 1, 1970 (UTC) at the moment the miner started hashing the block.
- **nBits**: The difficulty target. A miner must find a hash output of the block header that satisfies the following inequality: \(H(H(\text{Block header data fields}))<\text{nBits target difficulty}\). It is used to calculate a threshold that a block header has must be equal to or under in order to be appended to the blockchain.
- **Nonce**: To generate a new hash digest, we require new hash inputs. The nonce is one of the two values that normally change once the hashing of a block header begins. If the following \(HH((\text{Version} \Vert \text{Hash_Previous_Block} \Vert \text{Hash_Merkle_Root} \Vert \text{Time} \Vert \text{nBits} \Vert \text{Nonce})) < \text{nBits target difficulty}\) then the block is validated. If the inequality is not satisfied, the header is rehashed with \(\text{nonce}+1\). <span style="color:red">[the gif here works as an illustration](http://learnmeabitcoin.com/glossary/nonce)</span>
- **Transaction_List**: The data field containing all the transactions and other event data that we wish to append to the blockchain. Transaction data are hashed into the Hash_Merkle_Root <span style="color:red">as described here</span>.

An important concept here is the *block header*. The block header contains the following data fields: 1) Version, 2) Hash_Previous_Block, 3) Hash_Merkle_Root, 4) Time, 5) nBits, and 6) Nonce.

## A Nakamoto blockchain
Blocks are *chained* cryptographically. Each block header contains a reference to the previous block header (the Hash_Previous_Block data field).

**A pair of cryptographically chained Nakamoto blocks**
![](images/blockchainlink.png)

*Alternative image that also shows the Merkle Root.*
![](images/blockchainlinkroot.png)

The <span style="color:red"> transparent box that covers the left block CHANGE THIS TEXT DEPENDING ON IMAGE USED</span> indicates the parts of the block used as input data for the hashing that produces the data contained in the right block's Hash_Previous_Block data field. Here, we have a simple blockchain containing two blocks. However, the cryptographic link is the same regardless of how many blocks we append to the blockchain. Parts of each block header acts as data input to a hashing function that generates the value for the Hash_Previous_Block data field in the next block.

It is this cryptographic linking that makes transactions tamper proof on a blockchain&mdash;attempt to alter anything in a block, and the block header and its hash digest becomes altered and "breaks" the blockchain.

## A Nakamoto transaction
A transaction on a Nakamoto blockchain takes place generally follows these steps:
1. A node creates a transaction and signs it with its private key (<span style="color:red">there are special rules for how transactions are created and for what they contain, but more on that elsewhere</span>).
2. Signed, but yet unconfirmed, transactions are propagated to other nodes. If the transaction is valid (i.e., created following the rules) it is stored in the node's mempool.
3. Miners normally sort the mempool based on the transaction fee in each valid transaction. They then group the highest fee paying transactions and compute the Hash_Merkle_Root of the included transactions. They then try to mine the block.
4. Once a block is mined, that block is propagated on the network. The transaction is not confirmed and appended to the blockchain.
5. Additional blocks then further confirm the transaction. Each block increases the probability of the transaction being confirmed at a rate that depends on the [concentration of hashing power in the network](https://www.blockchain.com/en/pools) as can be [calculated here](https://people.xiph.org/~greg/attack_success.html).

Note that these steps may differ between various blockchain designs. For instance, certain blockchains provide immidiate confirmation of transactions (as opposed to the probabilistically increasing one in the Nakamoto design).

## Does your business need a blockchain?
Most likely, the answer is no. Blockchains do have great technical potential, but to this date much of this potential remains unrealized. We believe that the key to utilizing blockchain's technical potential is to 1) understand its technical benefits, 2) understand its context dependent nature, and 3) be able to select the right blockchain design for your context specific needs.

### Technical benefits
The benefits of blockchain technology are much discussed and highly praised (yet still surprisingly underutilized). The Nakamoto design was aimed at digital payments and value transactions, but its functionality can be applied in other contexts too. These benefits are as follows:

**Accounting**: In the Nakamoto design, outgoing transactions must reference incoming transactions. It is thus impossible to overspend tokens.

**Automation**: Many processes that would require human input can now be automated using conditional rule sets. This, is, arguably, true in general due to a broader digitalization trend. However, blockchain technology enables automated transactions between multiple parties in adversarial economic environments.

**Availability**: Permissionless open blockchain designs are highly available as the data state is replicated on many nodes. As long as a single node survives with the data state intact, everyone can verify it and restore it.

**Coordination point for economic activity**: Currently, many industries operate localized databases and data sharing throughout a value chain is troublesome. By design, blockchain technology relies on a shared source of trust among involved parties.

**Decentralized**: This is a core feature of blockchain technology. As mentioned in the definition, it enables distributed consensus around a shared data state *without the need* of a central coordinating authority or any third parties.

**Efficiency**: As there is no need for transaction verification, reconciliation, and clearing, overhead costs associated with transactions can drastically be reduced.

**Integrity**: A signed transaction cannot be modified, neither in part nor in full, without invalidating the digital signature and subsequently the transaction itself.

**Immutability**: Once enough time has elapsed after a confirmed transaction, it is extremely difficult to alter that transaction's confirmed state.

**Neutrality**: Permissionless blockchains proparage valid transactions regardless of who the participating actors are.

**Transparency**: Some blockchain designs, e.g., the Nakamoto design, are completely transparent. Everyone can browse the transaction history and verify the hash links. For instance, [you can browse and look for transactions on Bitcoin here](https://www.blockchain.com/explorer). This allows blockchains to be auditable.

**Trust**: Often claimed to be "trustless," blockchains offer guarantees that data on a blockchain, once confirmed, represents a shared view across a network. As long as events are purely digital, there is indeed no need to *trust* the data state, or that a smart contract will execute as the rule set details. This is, however, not necessarily true for blockchains that require some sort of cyberphysical linkage between real world events and digital representations.

**Secure**: The heavy use of cryptography secures all the transactions that are on a blockchain. Furthermore, the possibilities of attacking a permissioneless network are both expensive and rather limited in what they can accomplish <span style="color:red">as described here</span>.

Additional technical properties of the Nakamoto design can be found in [Andreas Antonopoulos' great book Mastering Bitcoin](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch12.asciidoc).

### The contextual characteristics of Blockchain technology
<span style="color:red">SHORT VERSION SO FAR ADD MORE LATER:
When to use Blockchains
1. Adversarial economic environment.
2. Purely digital OR digital twin possibility OR real benefits from data input transparency.
3. Interoperability and shared source of data state (many cases do not want themselves or wish others to manage a data infrastructure for all value partners).
4. Corrupt macro-institutions making it impossible to transact or exchange value without a decentralized mechanism.
5. Slow paced industries where delays offer possibility to not have to rely on CAP and finality.
When NOT to use blockchains
1. When alternative trust mechanisms are in place.
2. Where cyberphysical links are impossible to establish.
3. Where disintermediation becomes reintermediation.
</span>

### Selecting the right blockchain design for your needs
<span style="color:red">Take the table from the consensus algorithm part.</span>
