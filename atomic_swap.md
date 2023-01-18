What is Atomic swap?

Atomic swaps, also known as atomic cross-chain trading, is a technique that allows for the exchange of one cryptocurrency for another without the need for a 
centralised intermediary. This is achieved through the use of smart contracts on a blockchain. The atomic swap process is typically composed of two steps: the
setup of a hashed time-locked contract (HTLC) and the execution of the swap.

Applications:
-Decentralized exchange (DEX) trading
- between different blockchain networks
-Facilitation of cross-chain transactions

Advantages:
-Improved security and trustlessness by eliminating the need for centralised intermediaries
-Reduced counter-party risk
-Increased privacy by allowing for direct peer-to-peer trading

The technical implementation of atomic swaps involves the use of hash functions, which are mathematical functions that take an input (or “message”) and produce a
fixed-size string of characters, known as a “hash”. The hash function used in atomic swaps is typically the SHA-256 hash function, which is used in the Bitcoin protocol.

In the setup of an HTLC, the sender creates a contract that locks a certain amount of cryptocurrency A and assigns a unique hash value to it. The recipient must 
provide the secret key that corresponds to that hash value in order to unlock and claim the cryptocurrency A.
In the execution of the swap, the recipient then sends an equivalent amount of cryptocurrency B to the sender, who in turn provides the secret key to the recipient, 
allowing them to claim their cryptocurrency A.


In conclusion, atomic swaps are a powerful technique that allows for trust-less and decentralised exchange of cryptocurrencies across different blockchain networks.
By eliminating the need for centralised intermediaries, atomic swaps can improve security, reduce counter-party risk, and increase privacy in cross-chain transactions.
The use of hash functions and smart contracts is key to the technical
implementation of atomic swaps.
