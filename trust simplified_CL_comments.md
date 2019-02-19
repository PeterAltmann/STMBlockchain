# How blockchain enhances trust

It is easy to be confused about how blockchain technology relates to trust. Claims of the technology's ability to enhance trust are often as optimistic as they are vague about the details. Yes, blockchains do enhance *some* types of trust in *certain* contexts. No, blockchains do not replace our need for trust. Those that try to sell any other story are either is misinformed about the technology or, more likely, hope to bank on the hype and confusion. Illustrative examples are sadly not hard to find. The Economist's article on [The trust machine](https://www.economist.com/leaders/2015/10/31/the-trust-machine), Goldman Sach's piece [The New Technology of Trust](https://www.goldmansachs.com/insights/pages/blockchain/), the United Nations Development Programme's (UNDP) claim that ["we can trust people and organizations precisely because trust is no longer an issue"](https://www.blockchain.com/static/pdf/TheFutureisDecentralised.pdf), and IBM's general efforts in the space (see especially the [Food Trust](https://www.ibm.com/blockchain/solutions/food-trust) initiative) all misuse blockchains association to trust. Worse yet, the solutions they claim to build on blockchains often have few, if any, trust related benefits over something like Google Sheets.

The notion of trust in relation to blockchain technology is both fundamentally misunderstood and vastly exaggerated. To understand our position and how trust relates to blockchains, it is helpful to revisit the original [Bitcoin whitepaper](https://bitcoin.org/bitcoin.pdf) and contrast its use of the word 'trust' with how it is currently used in relation to blockchains. This is both concerning and unfortunate. Concerning in the sense that it may lead decision makers down a road where they assume trust exists while in fact it does not. Unfortunate in the sense that it is inimical to honest attempts to utilize actual blockchain technology to enhance trust.

## The concept of trust in Nakamoto's whitepaper

>Commerce on the Internet has come to rely almost exclusively on financial institutions serving as trusted third parties to process electronic payments [...]. What is needed is an electronic payment system based on cryptographic proof instead of trust. - [Nakamoto (2008)](https://bitcoin.org/bitcoin.pdf)

The above quote captures Nakamoto's original use of trust; a use that is limited to a (1) particular *type* of trust, (2) certain trusted *activity*, and (3) specific *context*. Trust in the context of blockchains referred to e-commerce, financial institutions, and the processing of electronic payments using cryptographic proofs. That is it. In fact, Nakamoto only intended to use cryptography to protect sellers, and never detailed how the buyer would be protected. Buyer protection is only mentioned in passing by arguing that "routine escrow mechanisms could easily be implemented to protect buyers."

Nakamoto's use of trust is today completely blown out of proportion. One reason to move beyond the original conceptualization of trust has to do with the development of general purpose blockchains, like Ethereum. Some lauded the development of such general purpose blockchains and erroneously claimed that all sorts of value exchanges are now possible without any third parties or trusted intermediaries. Whatever their reason for so doing, it has lead to the current situation where trust in relation to blockchains generally refers to one or more of the following categories:

1. trust related to digital payments
2. trust related to digital transactions
3. trust related to any value exchange (digital or physical)

Decision makers seeking to leverage the technical potential with blockchains, will benefit from quickly recognizing which particular category their trust enhancing efforts fall into. Failing to do so, will just lead to disappointment and hinder the exploration of suitable blockchain use cases. Next, we examine each category more in depth.

### Trust in the case of digital payments and digital transactions

Cryptographic proofs can only enhance trust in digital payments using a native token. Whether that token represents a currency, e.g., Bitcoin, or a digital asset, e.g., a CryptoKitty, matters not. What does matter is that there is no performance expectation that lies outside of the blockchain. If there is, things become complicated and the trust mechanism that Nakamoto designed simply does not apply. The example in Figure 1. serves to illustrates this claim.

**Figure 1.** Cryptographic proofs as a way to secure ledgers and digital transactions.

<span style="color:red">IMAGE ABOUT HERE WITH ALICE AND BOB BOTH HOLDING A COPY OF A LEDGER AND WHERE ALICE TRIES TO SEND A DIGITAL EVENT TICKET TO BOB AND WHERE BOB SENDS TOKENS TO ALICE AS PAYMENT. USE A LOCK IN A WAY THAT INDICATES THAT IT IS DIGITAL AND THAT IT SECURES THE LEDGER AND THE PAYMENT</span>

In **Figure 1.** Alice and Bob rely on cryptographic proofs to **secure their identical ledgers** and to **process a digital payments** (i.e., the token transfer) as well as the transfer of a **digital asset**, (i.e., the event ticket).

Breaking it all down, we have three different kind of value exchanges. Firstly, we have the transfer of a native token representing a currency. Secondly, we have the transfer of a native token representing the digital event ticket. So far so trustless. The third value exchange is a bit trickier. The event ticket represents an expectation of a future performance, i.e., the event. The vent is a performance expectation that lies outside of the blockchain. As such, the trust mechanisms that secured the token transfer do not apply (see Table 1. for the levels of trust involved in each of the cases).

**Table 1.** Trust in relation to different value exchanges

| Value exchange       | Details                                            | External input      | Trust required                             |
|----------------------|----------------------------------------------------|---------------------|--------------------------------------------|
| (1) Token transfer       | Cryptographic proofs secure token transfer process | No (self-referring) | The mathematical assumptions<br>The blockchain network                                       |
| (2) Digital event ticket | Digital asset representation                       | Possibly (colored coins), or <br>No (native token)      | Validity of data input and (1)                  |
| (3) Event performance    | Future performance in exchange for digital ticket  | Yes (physical)      | Performance honored<br>Asset transfer honored |

**The token transfer case**: The value transfer, i.e., the tokenized payment and asset representation, is processed using cryptographic proofs and there is no external data that needs to enter the blockchain. That is to say, the transfer is self-referring since the data state modification references an existing state on the blockchain&mdash;transfer this many tokens from this address to that address. In this case, we need to trust that the mathematical assumptions (e.g., Elliptic Curve Digital Signature Algorithm), the cryptographic assumptions (e.g., SHA / RIPEMD), and that the blockchain network is not compromised. While the two first are rather unproblematic, trusting that the network is working, and will work, as intended is a heavy assumption.

**The digital event ticket transfer**: This depends on whether we are using colored coins or a native token for asset representations. If we use a colored coin to represent a digital asset that exists elsewhere, we must trust that the digital ticket has not be used in another way, e.g., by being linked to another colored coin on some other blockchain. If we use a native token, then the trust mechanisms are the same as for the token transfer case above. In addition, we must now trust that the ticket is recognized as valid.

**The event performance**: The underlying performance expectation that the digital ticket represents is even more problematic still. A digital even ticket has value because it represents a performance  expectation that a buyer is willing to pay for. However, blockchain do not carry out performance expectations in the physical world. There is thus a need to trust that the event organizer recognizes the ownership transfer, grants the holder entry to the event, and that the event lives up to certain expectations.

Nakamoto's original intent to ensure 'trustless' digital payments is a far reach from claiming that blockchains ensure trust in all digital asset transfer. This is inadequately considered by proponents who believe that trust is removed in all digital transactions, or worse, in all kinds of value exchanges. Native token transfers already rely heavily on certain assumption (as outlined in **Table 1.**) that impact what we can trust and how we can trust it. Claiming that blockchains can enhance value exchanges in general when it comes to trust is naive at best, and malicious at worst.

### Moving trust out of the frying pan and into the fire

>The exchanges of value on which society is founded require us to trust each other’s claims about what we own, what we’re owed, and what we owe. To achieve that trust, we need a common system for keeping track of our transactions, a system that gives definition and order to society itself. The common thread between all of them is that mathematical rules and impregnable cryptography, rather than trust in fallible humans or institutions, are what guarantee the integrity of the ledger. [...] A blockchain [is] an electronic ledger—a list of transactions. Those transactions can in principle represent almost anything. They could be actual exchanges of money, as they are on the blockchains that underlie cryptocurrencies like Bitcoin. They could mark exchanges of other assets, such as digital stock certificates. They could represent instructions, such as orders to buy or sell a stock. They could include so-called smart contracts, which are computerized instructions to do something (e.g., buy a stock) if something else is true (the price of the stock has dropped below $10). - [Michael J. Casey and Paul Vigna (2018) in MIT Technology Review](https://www.technologyreview.com/s/610781/in-blockchain-we-trust/)

In the decade since Nakamoto's paper, the context of trust, the type of trust, and the trust related activities are all different. Meanwhile, the technology's trust enhancing potential remains largely unchanged. The MIT Technology Review quote illustrates several concerning developments:

1. They move far beyond electronic payments and now include all digital assets and instruction sets
2. They move beyond financial institutions and here include all institutions
3. It is no longer clear who is protected and from what they are protected
4. The specific nature of data feeds (e.g., a stock's price) is not problematized
5. It is unclear how the buyer's intent is translated into an instruction
6. It is unclear how the buyer can know that the instruction set has executed

Number 1. to 3. on that list extend the scope of trust, or rather trustlessness, beyond payment reversals and financial institutions&mdash;Nakamoto's original context and trust mechanism&mdash;to include all economic activities and all economic actors. This boundary problem plagues the current discourse on trust related to blockchains and is highly misleading as it can create unreasonable expectations on blockchain's technical and commercial potential.

Number 4. requires one or more references to data points outside of the blockchain, i.e., we need a data feed. The issue here is that a blockchain is equally suitable for immutably storing a truth as it is immutably storing a falsehood. Any time a transaction requires a data input, trust enters the picture. Sadly, there are those that everything blockchain related is trustless by association.

Number 5. and 6. does not consider that a stock buyer would probably not inspect the smart contract, but rather trust its developer. In addition, a buyer would also need to trust an institution to enforce his or her ownership claim of the stock. Enforcing an asset ownership is difficult when we require a link between the digital and the physical. For instance, a digital stocks often represents an ownership stake in a physical company that generate profits from performances that exist in the physical world. Without being able to establish a cyberphysical link, blockchains are only as trustworthy as the mechanisms between the digital and the physical world.

The MIT Technology Review quote illustrates three of the most severe problems with the contemporary ways of viewing trust in relation to blockchains.:

1. The *associative problem*: Anything associated with blockchain is trustless, including the data feed, instruction set, and physical asset exchange
2. The *boundary problem*: Trust has been extended from digital payments to digital and physical value exchanges, from e-commerce to other trading platforms, from specific payment scripts to general purpose instruction sets
3. The *cyberphysical link problem*: Blockchains are only as trustless as the linking mechanism between the physical world and its digital representation and only as valuable as the ability to enforce this link

The associative problem, the boundary problem, and the cyberphysical link problem are inadequately considered in many blockchain related texts and promises, for instance:

>[The] values of security, decentralization, privacy and transparency offer the most profound quality of blockchain: trustlessness&mdash;a model that does not require trust to safely interact and transact. [A] trustless paradigm, one where trust is not even needed as the system itself is immutable and incorruptible. - [Lisk Academy](https://lisk.io/academy/blockchain-basics/benefits-of-blockchain/blockchain-transparency-explained)

>The blockchain lets people who have no particular confidence in each other collaborate without having to go through a neutral central authority. - [The Economist (2015)](https://www.economist.com/leaders/2015/10/31/the-trust-machine)

>All these ‘trusted intermediaries’ are part of the world of institutional trust that is now being deeply questioned [...] third parties currently paid to facilitate our trust—be they agents, referees, watchdogs or custodians—will increasingly have to prove their value if they don’t want to be supplanted by an ‘immutable’ ledger. - [Rachel Botsman in Wired (2017)](https://www.wired.com/story/how-the-blockchain-is-redefining-trust/)

>Trust does not arise from the relationship between parties or through an intermediary but from the technology and the process of comparison in the network. [Blockchain is] a new platform of business relations that could become the new medium of economic trust - [Marcel Nicker at BearingPoint](https://www.bearingpoint.com/en/our-success/insights/trust-the-real-innovation-behind-blockchain/)

>[T]he blockchain is a “trust-free”, distributed solution that can be understood as techno-social system, where the technical part assures the transactions of the social part - [Roman Beck et al. (2016)](https://pdfs.semanticscholar.org/9a20/1289042464e21512119a27d2f6cfa8a67f5b.pdf)

Blockchains are often portrayed as if the technology can remove the need to trust any actor or institution, for all types of economic exchanges, both in the digital and the physical world. While the technology has evolved since 2008, the above claims are mere fantasies when taking into account what blockchains are presently capable of. And if the technology one day can live up to these expectations, there is no guarantee that blockchains will become anything but "outlaw technologies irrelevant to the mainstream economy" ([cf. Werbach, 2018](https://mitpress.mit.edu/books/blockchain-and-new-architecture-trust)).

Until now, we have argued that blockchains are not remotely as trustless as often claimed and hailed. However, blockchains invites us to reconsider the concept of trust. So, while decision makers are wise to be skeptical about grand claims of reducing the need to ever trust people again, they are also wise to consider how the particular type of trust blockchains introduce may impact their businesses.

## The roles and types of trust

>The blockchain does not create or eliminate trust. It merely converts trust from one form to another. - [Dirk Baur and Niels Van Quaquebeke](https://theconversation.com/the-blockchain-does-not-eliminate-the-need-for-trust-86481)

A Nakamoto blockchain shift the locus of trust from one financial institution to many independent nodes. A general purpose blockchain, like Ethereum, shifts the locus of trust from a single computer executing the instruction set to many independent nodes updating the data state according to a given procedure. In other words, blockchains shift trust from the few to the many. This design, together with validation/mining rewards, assumes that actors are self-serving and profit maximizing. It attempts to use individual greed to secure a collective good ([cf. Kasireddy's Medium article](https://medium.com/@preethikasireddy/eli5-what-do-we-mean-by-blockchains-are-trustless-aa420635d5f6)).

The focus on how blockchains shift trust from one to the many is a very commonly discussed benefit. However, the shift in locus is also the least interesting one in many ways. Trust is multifaceted [(Zucker, 1986)](http://psycnet.apa.org/record/1988-10420-001), and to understand how blockchains can impact trust, we need to understand what role trust plays in economic exchanges and what types of trust exist.

### Role I: Trust as a signal

Ironically, trust can arise from one actor signaling that there is no need for trust. For instance, we are more likely to trust the motives and actions of someone who is fully transparent and who can guarantee that no agreement is altered without everyones explicit consent. Since blockchains are so strongly associated with concepts like transparency, tamper resistance, provenance etc., they are often used by companies for signaling purposes (cf. the *associative problem* discussed above). For instance, banks can, and do, openly signal that they work with blockchains:

>The Corda platform is a cutting edge blockchain platform that removes costly friction in business transactions - [R3. website](https://www.r3.com/)

On their website, R3. makes generous use of keywords like "consensus", "provenance", "smart contracts", "immutability", and "interoperable blockchain," thus strengthening the association.

In reality, R3., and similar enterprise blockchains, have little in common with the projects that popularized those concepts, like Bitcoin and Ethereum. Solutions like R3. Corda rely on existing non-token based incentives, employ limited access rights, and require known and trusted validators to function. Such a design, is exactly what Nakamoto sought to avoid. However, technical similarities and differences do not matter for those who are not aware of [the many differences](https://medium.com/@micobo/technical-difference-between-ethereum-hyperledger-fabric-and-r3-corda-5a58d0a6e347) between R3.Corda and an actual blockchain.

The R3. Corda case is by no means an exception. For instance, IBM signals trustworthiness through their claim of using blockchains. They do this despite the fact that [their deployed solutions](https://arena.gov.au/assets/2017/10/Final-Report-MHC-AGL-IBM-P2P-DLT.pdf) have only the name "Blockchain" in common with actual blockchains and the rest is nothing but a traditional centrally managed database. Companies can, and will, signal that they are trustworthy by announcing a blockchain or distributed ledger technology project as long as the association exists.

### Role II: Trust as expectations and assumptions

Who would you trust between (i) a person who sets aside his or her self-interest both in favor of others' interest and in favor of the expectations of a collective, and (ii) a person who is greedy? Perhaps counterintuitively, blockchains favor (ii). Self-interest is intersubjective and universal, which makes it highly suitable as the foundation for an incentive for honest behavior. A miner secures and confirms payments on the blockchain by expending energy in exchange for tokens. It is easy to understand the motives of the actors involved.

However, as soon as the blockchain needs to refer to some external state&mdash;be it an asset representation or an event performance&mdash;it loses its intersubjective meaning. Worse yet, it now becomes harder to understand why someone would participate in the network. The rules are also harder to understand and value becomes subjective. All of a sudden, trust is based on something that depends on the source of the data input, the geographic location, and the cultural context that carries with it assumptions and expectations. Under such circumstances, it is a grave mistake to assume that performance expectations are easy to define and enforce.

General purpose blockchains introduce several issues related to trust. For instance, it is incorrect and dangerous to believe that trusting that a smart contract executes *equals* a trustless contract. It is also not true that trust in the data stored on the blockchain means that these data correctly mirror a physical reality. Finally, it is wrong to assume that the immutability of an asset representation means that this representation will be enforced or honored. Blockchain transactions that execute an arbitrary rule set often require a lot of trust. The exception is when performances are digital and refer to previous states on the blockchain, e.g., CryptoKitties.

### Types of trust

We need to distinguish between three types of trust:

1. Trust placed in institutions and professional roles
2. Trust based on signaled familiarity
3. Trust based on expectations and historic behavior

While blockchain technology offers several levels of trust as explained in **Table 1.**, it does not mean that people will trust it based on its technical potential. What people can trust and what people do trust are not the same. [Dirk Baur and Niels Van Quaquebeke](https://theconversation.com/the-blockchain-does-not-eliminate-the-need-for-trust-86481) point out that people find it difficult to trust the mathematics since they do not understand it. Thus, these people trust solutions depending on how they relate to key figures, e.g., Vitalik Buterin. So, while it is perfectly reasonable to claim that blockchains can enhance trust, the fact is that most people trust someone claiming that it is trustless. Similarly, people now conceptualize decade old technologies as trustless, despite these technologies having received nothing more than a facelift and had a new label slapped on them (e.g., R3., IBM, Oracle, etc.). Why? Because of how people trust rather than what people can trust.

Ironically, people may trust old rebranded technologies more than they trust the new novelties blockchains introduced despite the fact that the latter does not require trust in the same way as the old one did. A way to get around this is to create clarity in terms of how the different technologies actually differ. Blockchains are fair because the process involved in the value exchange is fair. Other technologies branded as blockchains are fair because some central entity says so. Blockchains enforce rules by design. Other technologies branded as blockchains enforce rules through institutional recourse. A general advice is that if there is a central actor who makes the claim that the blockchain solution they are offering is trustless, then it is not.

Blockchains can be trusted because of the transparency of the processes by which decisions are made ([cf. procedural justice](https://en.wikipedia.org/wiki/Procedural_justice)). It is a system that principally ensure trust through a process. Much like dice rolls can generate outcomes people accept because of a fair process, blockchains can enhance trust under certain circumstances (outlined in **Table 1.**) through a process.

How does the Nakamoto blockchain compare to the three types of trust above? Nakamoto designed blockchains specifically to avoid trust in institutions and professional roles. Signaled familiarity matters more for what people do trust related to blockchains than for what they can trust. And the expectations are simple: self interest and profit maximization. Instead, blockchains rely on **processual trust.** Blockchains ensure trust through an inclusive and transparent process by which outcomes are generated in a manner people consider fair. The rules of the protocol and the requirements for data state changes are public&mdash;people *can* know the rules of the game and what the payouts are.

##  Blockchain technology, trust, and the creation of business value

To understand how blockchains *can* enhance trust, we need to look closer at three trust mechanisms.

1. **Macro-institutional trust** where the locus of trust lies in banks, certificate systems, third party intermediaries, role expectations, courts and so on,
2. **Relational trust** where the locus of trust lies in social networks, reputation, informal rules and so on, and
3. **Processual trust** where the locus of trust lies in the activities by which something is determined.

The first is similar to the trust in institutions and professional roles discussed above. The second and third are different though when we focus on what we *can* trust. Processual trust what people colloquially refer to as 'trustless.' But above argued, processual trust is applicable only to Nakamoto's original intended use, i.e., digital payments using a native token. It has limited suitability for anything beyond that. Most importantly, processual trust has no technical potential to enhance trust if value transactions are linked to physical events or performances, unless the cyberphysical link is accurate and trustless. **Table 2.** summarizes this view.

**Table 2.** Blockchains and trust

|               | Self-referring           | External input           |
|---------------|--------------------------|--------------------------|
| Digital only  | Processual trust         | Depends on source        |
| Cyberphysical | All other types of trust | All other types of trust |

Until we figure out enforcement and digital mirroring, processual trust is still only possible for the kind of self-referring native token transfers bitcoin introduced (with the possible exception of interoperable blockchain token swaps). It is important to clarify what trust mechanism we can or should use for what part of the performance and the economic exchange we have in mind. Knowing the answer to that question can help us understand when blockchains provide real business value; or, perhaps more importantly, when it does not.
