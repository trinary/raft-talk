##  More Client Caveats

Read operations must also be answered by the **leader**, because stale data served to clients must be avoided.

***

At the start of its term, a **leader** doesn't necessarily know that all of its entries are committed.  So, to solidify the new **term**, a **leader** commits an empty entry immediately upon election.

Additionally, a **leader** may have been usurped without knowing. So, before answering any _read only request_, a **leader** must successfully issue a heartbeat to a majority of the cluster.

