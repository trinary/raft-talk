##  Log Replication

Only the **leader** issues _AppendEntry_ RPC calls to **followers**, and only the **leader** responds to client requests.

***

Client commands are appended to the **leader's** log, and then an _AppendEntry_ is issued to all **followers**.

***

A client request is committed if a majority of **followers** respond to the _AppendEntry_ call.

***

Failed _AppendEntry_ calls are repeated indefinitely, and the **term** and **index** of each call are included.

