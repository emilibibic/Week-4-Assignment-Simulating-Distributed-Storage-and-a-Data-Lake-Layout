# Cluster Design

## Architecture Overview
This cluster follows a standard Master/Worker architecture (similar to HDFS). 
*   **Master Node:** Manages the file system namespace and tracks which worker nodes hold which data blocks.
*   **Worker Nodes (DataNodes):** Store the physical data blocks and handle read/write requests from clients.

## Block Size and Replication
*   **Block Size:** 128 MB. This minimizes metadata overhead on the master node and optimizes sequential reads.
*   **Replication Factor:** 3. Every data block is duplicated across three separate worker nodes to ensure high availability and fault tolerance.