What’s New in Next Gen Corda?

The new architecture brings new components and concepts for Next Gen Corda.Introducing:

1. Event-driven workers : In Next Gen Corda, different worker processes are responsible for various aspects of running Corda, e.g., the flow workers execute flows and
verify contracts, and the DB workers handles interactions with the cluster database.
2. Virtual nodes : With Next Gen Corda, a Corda instance can host multiple virtual nodes. An instance of Corda is composed of a number of processes executing in
parallel to perform all of the required operations.
3. Application Networks: Each network has a set of applications packaged in a CPB (Corda package bundle). It also has a network ID and a network policy which are
bundled with the CPB into a CPI (Corda package installer).

To summarize what’s new in Next Gen Corda, it moves away from the monolith physical node engine architecture and adopts the agile setup where stateless event-driven 
workers can spawn on demand. By doing so, Corda can maximize the resource utilization for each virtual node. 
The network management is moved before CorDapp deployment with the help of CPIs, leaving less operational intervention post-deployment.
