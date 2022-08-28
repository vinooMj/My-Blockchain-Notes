DONs. Decentralized Oracle Networks. Hybrid smart contracts where on-chain code interacts with web2 servers to support dApps. 

Summary:

🔙 Background. Assume citizen X and Y want to place a bid on a home. X puts up $100k and Y puts up $100k. Both are placed in escrow via smart contract 
on-chain but to determine who wins the housing bid, we'd need to know the down payment percent, the interest rate, the credit scores and more. 
How will the smart contract know which citizen to allow to win the bid? The real world data and information requires an oracle mechanism to fetch 
accurate match outcomes off-chain and deliver it to the blockchain in a secure and reliable manner.

The Oracle Problem. Smart contracts (blockchain automation code) cannot interact with platforms outside of their native blockchain. 
Blockchains are purposely isolated in order to satisfy key use cases like: valid user transactions, mitigate downtime and prevent double-spending 
via a public ledger. This is where Oracles come in - they bridge a blockchain to an off-chain system.

Why Do We Need Oracles? Think of them as gateways to valuable data - data that needs to be connected to a blockchain like asset prices when 
pulling data for the weather, finance, insurance, ID verification, research, etc. That's why it is crucial that the Oracle works properly.

The Second Problem. Next - Oracles can be either centralized or decentralized .. if it's centralized, then the entire oracle can crash due to a 
single point of failure. It can also host poor data meaning the entire smart contract would have faulty outcomes. That's where DONs come in .. 
Decentralized Oracle Networks. These networks combine multiple independent oracle node operators and multiple reliable data sources to establish 
end-to-end decentralization.

⚙️ Main Types.
- Input Oracles (fetch data from the real world, on-chain, financial data)
- Output Oracles (send commands to trigger actions, off-chain, bank payment, pinging IoT system to unlock a car door once the on-chain payment is made
