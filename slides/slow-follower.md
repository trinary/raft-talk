##  A Slow Follower

If a leader has a very slow follower, it could take a snapshot and discard a log entry that the follower still needs.

***

A new RPC, _installSnapshot_, lets a leader catch a follower up to its last snapshot, where it will be able to continue replication.

***

When a **follower** recieves an _installSnapshot_ call, it must decide what to do with its existing log.
