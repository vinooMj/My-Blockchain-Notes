How to send a transaction signed by your own private key using a public RPC node? The node doesn’t know your private key, so you need to sign the transaction locally
- before sending it to the node. 

Here’s a simple guide how to configure your Truffle framework to connect to a public node but still sign the transactions locally.

1️⃣ Open the truffle-config.js file

2️⃣ Create a “networks” section and specify a name of the network. It can be pretty much any name, as it’s only used in your project and not validated against any
database. But it’s often good idea to stick to the traditional naming of those networks - mainnet, sepolia, mumbai, and so on.

3️⃣ And finally, under the "provider" property, pass HDWalletProvider object with your private keys and URL of your RPC node provider. Each private key is a
0x-prefixed string.

4️⃣ Now your Truffle framework can sign transactions from addresses that are derived from those private keys. 

This post is part of my series on Truffle suite / Ganache usage, best practices, and tips & tricks. Be sure to follow to not miss any future posts.
