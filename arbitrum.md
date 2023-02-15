inside  Arbitrum ; 1st Ethereum Scaling  L2 Solution

🔗Arbitrum is a suite of Ethereum scaling solutions that enables high-throughput, low cost smart contracts while remaining trustlessly secure. 
Arbitrum has three modes: AnyTrust Channels, AnyTrust Sidechains, and Arbitrum Rollup.


🔷It offers The following benefits : - 
🔹Trustless Security - Security rooted in Ethereum, with any one party abel to ensure correct Layer 2 results 
🔹Scalability - Moving contracts’ computation and storage off of the main Ethereum chain, allowing much higher throughput..

✅Arbitrum is a rollup, which means that the inputs to the chain -- the messages that are put into the inbox -- are all recorded on the 
Ethereum chain as calldata.

✔️Arbitrum is optimistic, which means that Arbitrum advances the state of its chain by letting any party (a “validator”) post a rollup block 
that that party claims is correct, and then giving everyone else a chance to challenge that claim. If the challenge period (roughly a week) 

passes and nobody has challenged the claimed rollup block, Arbitrum confirms the rollup block as correct. If somebody challenges the claim during 
the challenge period, then Arbitrum uses an efficient dispute resolution protocol (detailed below) to identify which party is lying. The liar will
forfeit a deposit, and the truth-teller will take part of that deposit as a reward for their efforts (some of the deposit is burned, guaranteeing 
that the liar is punished even if there's some collusion going on).

☞Among optimistic rollups, the most important design decision is how to resolve disputes. Arbitrum uses interactive proving, which we believe is 
more efficient and more flexible. The key principle behind interactive proving is that if Alice and Bob are in a dispute, Alice and Bob should do
as much off-chain work as possible needed to resolve their dispute, rather than putting that work onto an L1 contract.

🟨The Arbitrum Virtual Machine (AVM) is the interface between the Layer 1 and Layer 2 parts of Arbitrum. Layer 1 provides the AVM interface and
ensures correct execution of the virtual machine. Layer 2 runs on the AVM virtual machine and provides the functionality to deploy and run contracts, 
track balances, and all of the things a smart-contract-enabled blockchain needs to do.

🟡Every Arbitrum chain has a single AVM which does all of the computation and maintains all of the storage for everything that happens on the chain.

🟢Arbitrum rollups aim to maintain compatibility with Ethereum. Smart contracts are compatible on the bytecode level, but there are certain aspects 
of the system that work differently to the EVM.
