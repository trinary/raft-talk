##  Election

1. Each node increases its **Term** and moves to a Candidate state.
1. It votes for itself and issues a _RequestVote_ RPC to all other nodes.
1. One of three things can happen:
  * A given node gets successful Votes from a majority of the cluster and becomes the **leader**.
  * Another node idenitifies itself as a leader (by issuing a heartbeat with a larger **Term**), the others become **followers**.
  * A split vote results. After a timeout, another election is started.
