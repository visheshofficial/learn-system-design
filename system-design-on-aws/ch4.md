# Chapter 4. Caching Policies and Strategies

In computing, a cache is a component or mechanism used to store frequently accessed data or instructions closer to the processor, reducing the latency of retrieving the information from slower storage or external resources. Caches are typically implemented as high-speed, small-capacity memories located closer to the CPU than the main memory. The goal is to improve overall system performance by reducing the time required to access data or instructions.

Cache hit: data is found in the cache
Cache miss: data is not found in the cache

## Caching Benefits

- Faster access
- Reduced latency
- Bandwidth optimization
- Improved throughput

### Amdahl’s Law

Amdahl’s Law states that the overall speedup achieved by optimizing a particular component of a system is limited by the fraction of time that component is utilized

### Pareto Distribution

The Pareto distribution, also known as the 80/20 rule, states that a significant portion of the system’s workload is driven by a small fraction of the data

## Cache Eviction Policies

Cache eviction policies try to maximize the cache hit ratio.

### Belady’s Optimal Algorithm

Belady’s algorithm is an optimal caching algorithm that evicts the data item that will be used furthest in the future.
It acts as a benchmark for other caching algorithms.

### Queue based Eviction Policies

- First-In-First-Out (FIFO) - evicts the oldest item
- Last-In-First-Out (LIFO) - evicts the most recently added item. not commonly used

### Recency Based Eviction Policies

- Least Recently Used (LRU) - evicts the least recently used item
- Most Recently Used (MRU) - evicts the most recently used item.

### Frequency Based Eviction Policies

- Least Frequently Used (LFU) - evicts the least frequently used item.
- Least Frquently Recently Used (LFRU) - evicts the least frequently used item among the least recently used items.

## Allowlist Policy

An allowlist policy for cache replacement is a mechanism that defines a set of prioritized items eligible for retention in a cache when space is limited.

## Cache Invalidation

Cache invalidation is a crucial aspect of cache management that ensures the cached data remains consistent with the underlying data source

- Active Invalidation - invalidating the cache when the data is modified
- Invalidating on Modification -
- Invalidating on Read
- Time-to-Live (TTL)

## Caching Strategies

define how data is managed and synchronized between the cache and the underlying data source

 read-intensive caching strategies - focusing on optimizing the retrieval of data that is frequently read or accessed
 write-intensive caching strategies - optimizing the storage and management of data that is frequently updated or written

- Cache-Aside - managed by the application
- Read-Through - managed by the cache.. offloads the application
- Refresh-Ahead -
- Write-Through -  write to the cache and the underlying data source
- Write around - write to the underlying data source without updating the cache
- Write-Back - write to the cache and update the underlying data source asynchronously

## Caching Deployment

- In-process caching - cache is managed within the application process
- Inter-process caching - cache is managed by a separate process or service that is shared across multiple applications or services on the same host
- Remote caching - cache is managed by a separate process or service that is shared across multiple applications or services on different hosts

## Caching Mechanisms

- Client-side caching - caching data on the client side  (browser)
- CDN Caching - static content is cached on distributed servers
- Web Server Caching - server-side caching for frequently accessed content
- Application Caching - application memory or in-memory caching
- Database Caching - query level caching or object level caching

## Content Delivery Networks

 distribute and cache content across geographically distributed servers

push CDN - content is pushed to the edge servers
pull CDN - content is pulled from the origin server when requested

- CDN Optimization
  - Dynamic Content Caching Optimization
    - Content Fragmentation
    - Edge-Side Includes (ESI)
    - Content Personalization
  - Multi-tier CDN architecture
  - DNS Redirection
  - Client Multiplexing

Cache Consistency
    - Periodic Polling
    - Time-to-Live (TTL)
    - Leases

## Open Source Caching Solutions

- Memcached
- Redis
