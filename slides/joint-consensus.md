##  Joint Consensus

Properties of the _joint consensus_:

* Log entries are replicated to all servers in both configurations.
* Any server from either configuration can be elected **leader**.
* Agreement on things like election and log commits require separate majorities from both configurations.

***

Configurations are implemented as special log entries with index, term, and all the rest. They are sent to the **Leader** and replicated to the **followers**.

***

**Followers** can begin using a new configuration (list of member machines) immediately.
