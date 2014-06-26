##  Overview

Raft describes how systems elect a leader, issue log writes to the followers, and transition between states and configurations.

***

It makes some guarantees:

* When there's an election, only one node will win
* Leaders only append their own log entries, never overwrite them
* If two logs have a particular entry, they match up to that point
* If a log entry is committed, all future leaders will have it
* Only one log entry with a particular index will ever exist
