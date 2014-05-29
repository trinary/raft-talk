##  installSnapshot

_installSnapshot_ can send a **follower** a complete or partial state.

Included with the call are the leader's **term**, the current leader's ID, the last included **term** and **index** of the **snapshot**

***

* If the **term** or **index** of the leader and snapshot are older than what the **follower** already has, it can ignore the call.

* Otherwise, it can write the **snapshot** to disk and discard all entries in its log that the **snapshot** accounts for.

* If the **snapshot** includes new data, the **follower** can replace its entire log.

* If the **leader** has sent its entire **snapshot**, it can set a flag in the last call to tell the **follower** that it is up to date.
