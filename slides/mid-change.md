##  Changing Membership

During a configuration change, new nodes can be added and existing nodes removed. Some special behavior can account for these changes safely.

***

* New servers with an empty log are _non-voting_ until they get caught up, this phase occurs before the leader commits the _joint consensus_ config.
* If an existing leader is being removed (its own id is not in the member list), it steps down as leader.
* To prevent removed nodes from disrupting the cluster by sending _requestVote_ calls, candidates will always refuse a vote until they reach their heartbeat timeout.
