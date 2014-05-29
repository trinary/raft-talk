##  Leader Election

All log writes are done through a **leader**. A single node is chosen as the leader for a given **term**.

***

The **term** is a monotonically increasing counter, which is included as a property of all RPCs.

***

The **Leader** sends **heartbeat** messages to all reachable nodes, in the form of an _appendEntry_ RPC with no data.

***

If a **follower** doesn't hear from its **leader** for a pre-set time, an **election** is triggered.

