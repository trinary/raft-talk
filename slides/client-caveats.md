##  Client Caveats

There are some subtleties to client behavior that the system needs to account for.

If a **leader** crashes after committing a command but before responding to the client, the command will be repeated.

***

The duplicate command in this case would have a new **index**, potentially overwriting valid state.

To get around this, the state of the system must include an identifier for each client, and a serial number for each command as part of the state of the log.

If any command comes in to any node with an index that it has already seen, the command is ignored.
