##  Clients!

So how do clients of a Raft system act?

***

All clients send all of their requests to the **leader**. They find the **leader** by connecting to a random node.

If that node isn't the **leader**, it tells the client about the **leader** it knows about.

If a **leader** crashes and a client request fails, the client should try a random node next.
