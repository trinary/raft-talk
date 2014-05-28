##  Safety Proof

With these restrictions on _appendEntry_ and _requestVote_, we can attempt to prove that elected **Leaders** have a complete log:

***

1. Given a committed entry (majority of servers accepted the _appendEntry_)
1. And an elected leader with a log that does not contain that entry (majority of servers gave a vote)
1. There must be at least one server that granted a vote to a system with a less up-to-date log than its own.
