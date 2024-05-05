# Chapter 1. System Design Trade-offs and Guidelines

## System Design Concepts

- Communication
  - exchange of information and data
  - synchronous or asynchronous

- Consistency
  - distributed systems - all replicas or servers having the same view of the data
  - data storarage - each read receives the most recent write or an error
  - Consistency in distributed systems
    - Data Replication
    - consensus algorithms
    - conflict resolution
  - Consistency in data storage and retrieval
    - Writing ahead logging
    - Locking
    - Data versioning
  - Consistency Spectrum Model
    - Strong Consistency
    - monotonic read consistency
    - monotonic write consistency
    - causal consistency
    - eventual consistency

- Availability
  - system is able to process requests and return responses in a timely manner even when some of its components are failing or errors are occurring
  - Measuing availability
    - availability% = (total time - downtime) / total time
    - goal is to maximize availabilitygo
    - availability becomes progressively challenging  and resource intensive as the target availability increases
  - avaialbility in parallel vs in sequence
  - ensuring availability
    - redundancy
    - fault tolerance
    - load balancing
  - availabiity patterns
    - Failover Pattern
      - active-passive
      - active-active
  - replication pattern
    - multi leader
    - single leader

- Reliability
reliability refers to the ability of a system or component to perform its intended function consistently and without failure over a given period of time.
  - measuring reliability
    - Mean Time Between Failures (MTBF)
    - Mean Time To Repair (MTTR)
    - Availability = MTBF / (MTBF + MTTR)

- Scalability
  - ability of a system to handle a growing amount of work or its potential to accommodate growth
  - types of scalability
    - horizontal scalability
    - vertical scalability

- Maintainability
  - ability of a system to undergo changes, updates, and modifications with ease
  - maintainability factors
    - operability
    - simplicity
    - Modifiability
- Fault Tolerance
  - ability of a system to continue operating in the event of a failure
  - Replication
  -Checkpointing
    - Sync Checkpointing
    - Async Checkpointing

## Fallacies of Distributed Computing

- Reliable networks
- Zero latency
- Infinite bandwidth
- Secure networks
- Fixed topology
- Single administator
- Zero transport cost
- Homogeneous systems

## System Design Trade-offs

- Time vs Space
  - MEMORY vs CPU
- Latency vs Throughput
  - Latency - time taken to serve a request
  - Throughput - number of requests served in a given time
  - inverse relationship between latency and throughput
  - metrics is through percentiles

- Performance vs Scalability
  -

- Availability vs Consistency
  - CAP Theorem
    - Consistency
    - Availability
    - Partition Tolerance

## System Design Guidelines

- Guideline of Isolation: Build It Modularly
- Guideline of Simplicity: Keep it Simple, Silly
- Guideline of Performance: Metrics Don’t Lie
- Guideline of Tradeoffs: There Is No Such Thing As A Free Lunch
- Guideline of Use Cases: It Always Depends
