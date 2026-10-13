# Failure Simulation

## Scenario: Worker Node 2 Crashes
If Worker Node 2 experiences a hard drive failure and goes offline, the following sequence occurs:

1.  **Heartbeat Loss:** The Master Node stops receiving the periodic "heartbeat" signal from Worker Node 2.
2.  **Under-replicated Blocks Identified:** The Master checks its metadata and identifies all blocks that were stored on Node 2. Their replication factor has now dropped from 3 to 2.
3.  **Replication Triggered:** The Master commands the surviving nodes holding the remaining replicas to copy those blocks to other active nodes (e.g., Worker Node 4 and 5).
4.  **Restoration:** The system returns to a stable state with a replication factor of 3 for all blocks, completely transparent to the end user.