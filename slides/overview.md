##  Overview

Raft describes how systems elect a leader, issue log writes to the followers, and transition between states and configurations.

***

It makes some guarantees:

* One leader at a time
* Leaders only appends log entries
* If two logs have a particular entry, they match up to that point
* If a log entry is committed, all future leaders will have it
* Only one log entry with a particular index will ever exist
