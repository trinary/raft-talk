##  Split Votes

But if every node enters the **candidate** state at the same time and the vote timeout is the same, won't they split the vote forever by voting for themselves at the same time?

***

This is where Raft opts for understandability over deterministic behavior.  The vote timeout is random, so the chance for a repeated split vote is very small.

***

One node will re-issue a _requestVote_ RPC (with a larger **term**) before the others time out, getting the first shot at the next **leadership**.

