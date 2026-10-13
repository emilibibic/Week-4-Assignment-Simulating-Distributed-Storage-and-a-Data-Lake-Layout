# Data Integrity at Scale

When storing petabytes of data, hardware degradation or network flips will inevitably corrupt bits of data. Distributed systems handle this silently through **checksums**. 

When a client writes a block of data, it also computes a cryptographic checksum (like CRC32) and stores it alongside the block. When the data is read later, the worker node recalculates the checksum. If the newly calculated checksum does not match the stored checksum, the system knows the data is corrupted. The master node will then discard the corrupted block and fetch a healthy replica from another node.