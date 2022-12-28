Trying to clear a few misconceptions around #ethereum sharding or 'surge' #ethereumsurge upgrade in simple terms without going down the technical rabbit hole:

1. Stop calling it ETH2. Ethereum's latest roadmap talks about a set of upgrades which will take decades to finish, ultimately making the network more scalable and 
censorship resistant.

2. The original design of 64 shard chains has been discarded. The new 'rollup-centric' design is called #danksharding (named after #eth researcher Dankrad Feist). 
This is nothing like horizontal #database #sharding in system design.

3. #rollups are #layer2 L2 technologies which batch transactions off-chain and submit some kind of proof to #layer1 that the state transitions are valid. They scale L1
while leveraging L1's security guarantees of #decentralization. The latest design enables rollups to scale instead of scaling the L1 directly.

For the sceptics: Internet is also made up of layers.

4. Main idea of Danksharding is seperation of powers between builders and proposers/validators. In PBS (proposer-builder seperation), specialised builders build blocks 
and validators propose and validate blocks in a secure way using a #cryptography technique called DAS (data availability sampling).

#vitalikbuterin Endgame article describes how all roads lead to centralized block production with decentralised validation: https://lnkd.in/dCgiyuM2

5. Rollups will require a lot of data to be posted on L1. Danksharding introduces blob data carrying transaction which attaches few KBs of data to blocks. This Blob data 
is what is sharded into smaller pieces, not the entire chain.

6. DAS allows nodes (even light clients) to easily and securely verify that blob data is available without downloading all of it (only 50%). This is achieved using 
#cryptographic gadgets called Erasure Coding and KZG Commitments. (I will explain both in future posts).

7. L1 does not interpret blob data. Only Rollups can directly access blob data, EVM can only access the commitments to it. Once enough validators have downloaded, 
reconstructed and validated blob shards, the data will be removed (probably after months) now that proofs are available that L2 state changes are valid. This turns
#ethereumblockchain into a settlement layer that ensures data availability while shipping off execution to L2s.

8. These are huge changes at protocol level and will take years to go live. EIP-4844 (Proto-danksharding) incrementally introduces some of these changes before the
full blown Danksharding.

So in summary:

Ethereum 'Surge' Sharding = PBS + DAS

Deliberately kept this very high level. Interested Ethereum developers can jump into details using below links by Vitalik
