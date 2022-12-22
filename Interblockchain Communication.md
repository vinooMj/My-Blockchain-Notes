There are 100s of blockchains but how do they communicate with each other?

One way is through bridges.

But apparently, more than 50% of the hacks have been through hacking bridges.

It's not that safe.

The other way through which Blockchains can communicate with each other is through IBC.

Interblockchain Communication is a standard messaging protocol that helps two completely independent chains with different consensus communicate with each other.

Let's understand how IBC works⬇

IBC consists of two layers.
1. Transportation, Authentication and ordering layer which is the base layer.

2. Application layer that is built on the top of TAO.

Suppose I lock up assets on Chain A and it needs to be verified on Chain B.

Chain A sends a message to Chain B.

Chain B verifies are the assets locked up or not on chain A through a light client (light client helps to generate a small proof that the transaction happened on
blockchain A)

The information is transferred in form of packets through Relayers via channels that have a smart contract connection at each end, so a data packet sent via a channel
proves that the data was sent from that specific smart contract affiliated with the blockchain sender.

One of the chains that use IBC is Cosmos.

