##  Safety Part One

Given that there can only be one **leader** at a time, and **term** and **index** increase monotonically, it follows that:

 * in any log, an entry with the same **term** and **index** will have the same data.
 * if any two logs have an entry with the same **term** and **index**, all preceeding entries are identical.

 ***

 The second property is ensured by a consistency check in the _appendEntry_ RPC. The leader sends the **term** and **index** of the entry preceeding the new entry. If the **follower** doesn't have that entry in its index, it rejects the call.

 ***

 If followers get an _appendEntry_ that conflicts with an existing entry, the new data wins. (_continued_)
