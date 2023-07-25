WHAT ARE NODES AND CLIENTS?

👨‍💻 A "node" is any instance of Ethereum client software that is connected to other computers also running Ethereum software, forming a network.
A client is an implementation of Ethereum that verifies data against the protocol rules and keeps the network secure.

👨‍💻 Post-Merge Ethereum consists of two parts: the execution layer and the consensus layer. Both layers are run by different client software. On this page, we'll refer to them as the execution client and consensus client.

👨‍💻The execution client (also known as the Execution Engine, EL client or formerly the Eth1 client) listens to new transactions 
broadcasted in the network, executes them in EVM, and holds the latest state and database of all current Ethereum data.
 
👨‍💻 The consensus client (also known as the Beacon Node, CL client or formerly the Eth2 client) implements the proof-of-stake consensus 
algorithm, which enables the network to achieve agreement based on validated data from the execution client.

👨‍💻 Before The Merge, consensus and execution layer were separate networks, with all transactions and user activity on the Ethereum 
happening at what is now the execution layer. One client software provided both execution environment and consensus verification of 
blocks produced by miners. The consensus layer, the Beacon Chain, has been running separately since December 2020. It introduced 
proof-of-stake and coordinated the network of validators based on data from the Ethereum network.

👨‍💻 With the Merge, Ethereum transitions to proof-of-stake by connecting these networks. Execution and consensus clients work together 
to verify Ethereum's state.
Modular design with various software pieces working together is called encapsulated complexity
(opens in a new tab)

↗. This approach makes it easier to execute The Merge seamlessly and enables the reuse of individual clients, for example, in the layer 2 
ecosystem. 

Blockchain Nodes

Node is a computer that runs the Blockchain Software to validate and store the complete history of transactions and of course the transactions are bundled into BLOCKS. 

Node is a computer that is connected to the Blockchain Network that has necessary software installed on it. 

Nodes are responsible for validating transactions, storing a copy of the Blockchain and replaying information to other nodes in the network.

Blockchain Nodes constantly exchange the information on new transactions and blocks. 

Different layers of Blockchain Node:

Applications & UI
 🔻 
APIs
 🔻 
Keys and Assets
 🔻 
Blockchain Frameworks
 🔻 
Operating System


There are different types of Nodes. I will present a few briefly. 

Archival Full Nodes:
These Nodes host the entire Blockchain, validate Blocks and maintain Consensus. 

Pruned Full Nodes:
This kind of Nodes initially download the entire Blockchain and then delete the blocks beginning with the oldest block till it holds the most recent transactions up to the size limit set by the operator. 

Master Nodes:
User who runs these nodes earn network rewards. These are typically used in Proof Of Stake (PoS) Blockchain Network such as Ethereum. Master Nodes are responsible for validating transactions, processing blocks and managing network governance. 

Cold Nodes: 
These are used for signing transactions offline and store the private keys away from the network. 

Lightning Nodes:
These nodes reduce the load on the network by enabling off chain transactions and these nodes enable faster and cheaper transactions. 
For example, in a country called 'el salvador' people can buy Pizza with BTC. So there these lightning nodes are used for BTC transactions.

