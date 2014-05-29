##  The Change Process

There are several phases to the change process.

First, a configuration describing the _joint consensus_ is created and replicated to **followers**.

***

This configuration establishes that both the old and new configurations are needed to commit or elect.

Once that is committed, the leader is able to create a config describing the final state and commit it.
