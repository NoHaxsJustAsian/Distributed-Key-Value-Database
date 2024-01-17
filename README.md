* Tunwa Tongtawee & Joseph Pierre-Louis - CS3700 - 12/10/2023*
# Project 6 - Distributed Key-Value Database

## Introduction
For our CS3700 course, we have developed a Distributed Key-Value Database. This project focuses on achieving consistent replication in a network using the Raft consensus protocol, and is designed to maintain strong consistency and high availability even in challenging network conditions.

## System Overview

Our key-value database is designed to support basic `put(key, value)` and `get(key)` operations, replicating these operations across multiple instances to ensure data integrity and availability.

### Raft Protocol Implementation
- **Leader Election:** Implemented the leader election part of the Raft protocol to handle failovers and maintain a single, consistent view of the data store.
- **Log Replication:** Ensured that all changes to the data store are replicated across all instances, keeping the data consistent across the cluster.
- **Commit Mechanism:** Implemented a commit mechanism where changes are only made permanent once a majority of instances have replicated the data.

### Optimizations
- **Efficient Messaging:** Reduced network overhead by optimizing the messaging system, ensuring that only necessary messages are sent and processed.
- **Batch Processing:** Implemented batch processing in the log replication phase to improve throughput and reduce latency.
- **Failure Handling:** Developed robust mechanisms to handle network partitions and instance failures, ensuring the system continues to operate effectively under various network scenarios.

## Usage

To interact with the distributed key-value database, users can perform the following operations:

- `put(key, value)`: Stores a key-value pair in the database.
- `get(key)`: Retrieves the value associated with a given key.

## Testing and Validation

- We utilized a simulator provided by the course to emulate client interactions and network conditions.
- Testing involved monitoring replica behavior, ensuring the Raft protocol was correctly implemented, and validating the system's response to simulated network disruptions.

## Future Enhancements

- **Scalability Improvements:** Further tuning to handle larger clusters and higher load.
- **Advanced Client Operations:** Adding support for more complex operations and queries.

## Acknowledgments

- Professor Alden Jackson and TAs of the CS3700 course for their guidance and support.
- Northeastern University for providing the resources and environment conducive to hands-on learning in networks and distributed systems.

---

*Note: This project was developed for educational purposes and demonstrates the practical implementation of distributed systems concepts.*
