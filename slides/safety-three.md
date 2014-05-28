##  Safety Three

Even maintaining _lastIndex_ is not enough.

What if an inconsistent **follower** is elected?

***

We require an additional constraint on election. The _requestVote_ RPC includes the **term** and **size** of the candidate's log, and if the recipient has a more up-to-date log, it denies the vote request.

***

Up-to-dateness is defined as:

* the log with the larger term is more up-to-date
* if the terms agree, the longer log is more up-to-date
* if both are equal, the candidates have the same log, and a vote can be granted.


