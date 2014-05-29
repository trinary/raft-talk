## Snapshots

A **snapshot** is a complete copy of the current state of a log, written to durable storage. Once written, the log up to that point can be discarded. Any node in a Raft system can take its own **snapshot** at any time.

***

Some metadata is written with the **snapshot**, like the last included **index** and the last included **term**. By keeping these values, subsequent _appendEntry_ calls can be satisfied. 

***

The last **configuration** is kept as well to deal with reconfiguration events.

