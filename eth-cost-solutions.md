Ethereum has a problem. It's too costly for your average person to participate in validating and verifying the network.

Good thing Ethereum's roadmap outlines how this will be resolved.

Ryan West takes you step-by-step through the Verge and the Purge will solve this.

- The Verge refers to the goal of having block verification be as easy and as light as possible.
- The Purge refers to the goal of simplifying the protocol by lowering the storage requirements to participate in validating the network.

1/ The Verge

It aims at making light clients as easy to run as possible and increasing their impact on the security guarantees of the protocol.
The Verge focuses on the inclusion of Verkle trees and SNARKs.
Merkle-Patricia trees, a modified version of Merkle trees, allow for the secure verification of a large number of transactions in a block. 
Ethereum is exploring a more efficient alternative to Merkle trees specifically for state, called Verkle trees.

Verkle trees
They look similar to Merkle trees, but rather than needing to provide every sister node on the way down to the node of choice, you instead just provide *the path 
itself* 

as part of the proof.
On their own, Verkle proofs are 3x more efficient than Merkle proofs.Combining all possible Verkle proofs of one tree into one SNARK increases this efficiency
exponentially.

SNARKify Ethereum
SNARKs are a version of zk proofs that allow one party to prove to another that something is true without revealing any information beyond the validity itself,
while allowing the verification to be as quick as possible and requiring little resources.

2/ The Purge
It refers to simplifying the protocol so that it becomes more viable to run a full node/validator. This comes primarily through the expiration and management of 
history and state.

As a reminder, history and state are two separate things. History, accounts for the entire past data of the chain. State is simply a snapshot of all the data 
needed to validate the chain at the current block, such as the balances of EOAs and smart contracts.

History Expiry (EIP-4444)

Historical data takes up a significant amount of hardware space for nodes. Currently, Ethereum’s history accounts for around 2.5 TB in storage per year, with Danksharding potentially bringing that number to 40TB per year.

State Expiry

Along with needing to download the entire history of the chain, full nodes also need to keep track of the state to know whether transactions have been valid. As more wallets and smart contracts use Ethereum, the state to keep track of grows exponentially larger.
