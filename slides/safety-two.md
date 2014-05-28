##  Safety Two

How does an inconsistent **follower** get brought back into line?

***

A **leader** maintains a _lastIndex_ for each follower, initialized to the last **index** in its log at election.

If a **follower** rejects an _AppendEntry_ call, the leader decrements this value and tries again. Eventually they agree and the **leader** issues _AppendEntry_ calls and increases that **follower's** _lastIndex_.

*** 

That's not the whole story, More Safety info to come!
