Orderer
An ordering service allows peers to focus on validating transactions and committing them to the ledger. 

Order the transactions
 
Cut the block and distribute the block amongst the orgs when the criteria is met ( min txn/size or time).
 
 orderer whose is responsible for receiving endorsed transactions from peers and put them into blocks then these blocks are distributed to all peers. 
 
 These blocks are Final.


Raft Consensus for production network

The sample network uses a single node Raft ordering service that is operated by the orderer organization. You can see the ordering node running on 
your machine as orderer.example.com. While the test network only uses a single node ordering service, a production network would have multiple ordering 
nodes, operated by one or multiple orderer organizations. The different ordering nodes would use the Raft consensus algorithm to come to agreement on 
the order of transactions across the network.

Their design allows different organizations to contribute nodes to a distributed ordering service.

Raft protocol uses a “leader and follower” model.

General orderer count is five. 

At least 1 orderer in your HLF network to work.	

Not every peer needs to be connected to an orderer - peers can cascade blocks to other peers using the gossip protocol.

Query is not a transaction which writes into the ledger. So it doesn't need the orderer. For query, it will pick up the data from the peer's 
local database.


Orderer Count:

While it's possible to use the console to build a configuration of any number of ordering nodes (no configuration is explicitly restricted), some 
numbers provide a better balance between cost and performance than others. The reason for this lies in satisfying the needs of high availability (HA) 
and in understanding the Raft concept of the "quorum", the minimum number of nodes that must be available (out of the total number) for the ordering 
service to process transactions.
 
In Raft, a majority of the total number of nodes is needed to form a quorum. In other words, if you have one node, you need that node available to 
have a quorum, because the majority of one is one. Similarly, if you have two nodes, you will need both available, since the majority of 
two is two (for this reason, a configuration of two nodes is discouraged; there is no advantage to a two node configuration). In a similar vein, 
the majority of three is two, the majority of four is three, the majority of five is three, and so on.
 
While satisfying the quorum will make sure the ordering service is functioning, production networks also have to think about deployment 
configurations that are highly available (in other words, configurations in which the loss of a certain number of nodes can be tolerated by the system). 
Typically, this means tolerating two nodes failing: one node going down during a normal maintenance cycle, and another going down for any other 
reason (such as a power outage or error).
 
This is why five nodes is a good number for a production network. Recall that the majority of five is three. This means that in a five node configuration, the loss of two nodes can be tolerated. If your configuration features four nodes, only one node can be down for any reason before another node going down means a quorum has been lost and the ordering service will stop processing transactions.
 
Ex:
 
Three orderer peer
 
I have solved this in such a way that in my case I have three orderers that run independently on different environments. If I crash all these orderers,
the peer containers will continue to run on the other participants of the network. As you said, they cannot make any transactions. If one of my orderers 
crashes it is not so bad after the raft consensus, the containers keep running. If another one fails, no transactions can be made. In this case 
I let the peers continue and check if the orderers are available again.
 
