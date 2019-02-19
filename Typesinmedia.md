# Blockchain types
Today, there exist many different types of blockchains (and possibly more definitions for each type than there exists blockchain types). Each blockchain has its own characteristics; some distinct to the particular blockchain, others overlapping with other blockchains.

Existing media uses three different ways to categorize blockchains.

## Categorization I: Distributed databases, distributed ledgers, and blockchains
Here, we use the following definition: Blockchains ⊊ Distributed ledgers ⊊ Distributed databases. Put differently:
>All blockchains are distributed ledgers, but not all distributed ledgers are blockchains. All distributed ledgers are distributed databases, but not all distributed databases are blockchains.

To understand their distinction, let us define each term:
- A **distributed database** is an umbrella term for databases where information is stored and processed throughout an interconnected network of nodes.
- A **distributed ledger** is an umbrella term for all kinds of distributed databases that do not require a central coordinator and where the participating nodes do not necessarily trust each other.
- A **blockchain** is a distributed ledger where the data structure is made up of <span style="color:red">blocks containing transactions</span> and where the data structure contains an economic incentive to govern behavior.

The key thing to keep in mind here is that a blockchain is a data structure. Specifically, it is an ordered back-linked list of blocks containing transaction data. Each block has its own hash identifier and is linked to each preceding block using a <span style="color:red">hash link</span>.

In contrast, distributed ledgers can employ data structures other than blockchains. Two common ones, that are often discussed along with blockchain, are Hashgraphs and Tangle. <span style="color:red">See https://techstartups.com/wp-content/uploads/2018/03/Distributed-ledger-technologies-in-comparison-.png for differences, if for nothing else than the graphics used to illustrate the data structure. We will return to these differences elsewhere</span>.

The above provides a quick overview. [Sebastien Meunier has a great post on Medium](https://medium.com/@sbmeunier/blockchain-technology-a-very-special-kind-of-distributed-database-e63d00781118) that explores the differences between distributed databases, distributed ledgers, and blockchains (as well as Hashgraphs and Tangle) and their particular use cases. See also [Richard Brown's forum post on the differences between distributed databases and Corda](https://gendal.me/2016/11/08/on-distributed-databases-and-distributed-ledgers/), which is a permissioned distributed ledger.

## Categorization II: Permissionless and permissioned blockchains.
Permissionless blockchains are public, i.e., not owned by anyone. Anyone can participate as a node in the network as long as they adhere to the protocol rules. In contrast, permissioned blockchains are only open to a consortium or small group of nodes that are run by organizations who want to share a ledger between them.

Some comparing images for inspiration:
- [Validator trust and anonymity sorted 1](https://cdn-images-1.medium.com/max/1600/1*HH1d22mqtWwlRTqOXawaoA.png)
- [Validator trust and anonymity sorted 2](https://blockchainhub.net/wp-content/uploads/2016/07/2.jpg)
- [Comparing table that also focuses on innovation target](https://cdn-images-1.medium.com/max/654/0*9N5oRmZEk6dQ9bAQ.png)
- [Compares native to non native token](https://masdeena.files.wordpress.com/2017/02/slide007.jpg)

https://blockchainhub.net/blockchains-and-distributed-ledger-technologies-in-general/ <span style="color:red">is a great source for information for this part of the text.</span>

## Categorization III: Native asset and representative asset blockchains.
Native asset blockchains are those that generate a value token (e.g., a cryptocurrency) as a result from some distribution mechanism (e.g., mining). Some blockchains, however, do not rely on native assets as an incentive mechanisms. These blockchains, here referred to as representative asset blockchains, do not require a token and often do not use tokens as a unit of value.

Instead, representative asset blockchains utilize blockchains technical benefits, e.g., immutability, security, consensus models etc., to share data between network participants. However, in omitting the native asset, representative asset blockchains often need another mechanism to incentivize honest behavior. Most often, this is achieved by relying on known identities and the threat of legal action.
