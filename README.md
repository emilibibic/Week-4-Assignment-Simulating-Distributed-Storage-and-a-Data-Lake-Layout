# Week 4: Distributed Storage and Data Lakes

## Overview
This repository simulates the foundational concepts of distributed storage systems. It includes designs for block replication, failure recovery mechanisms, and an optimized data lake layout for efficient querying.

## File Guide
*   `cluster_design.md`: Explains the Master/Worker architecture and block replication strategy.
*   `failure_simulation.md`: Details the recovery process when a node goes offline.
*   `lake_design.md`: Outlines the Hive-style directory partitioning (year/month).
*   `week4_queries.sql`: DuckDB queries demonstrating partition pruning.
*   `integrity_reflection.md`: Explains checksums and data corruption handling.

## Running the Queries
To run the SQL file:
1. Install DuckDB locally.
2. Execute `duckdb < week4_queries.sql`.