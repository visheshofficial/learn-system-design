# Chapter 2. Storage Types and Relation Stores

## Data Storage Formats

File Storage

- File storage is a method of storing data in a hierarchical structure.
- used for storing unstructured data, such as text files, images, videos, and audio files.
- AWS Elastic File System (EFS) is a managed file storage service that can be used to store and access files from multiple EC2 instances.

Block Storage

- Block storage is a method of storing data in fixed-sized chunks called blocks.
- stored on disk or flash memory
- AWS Elastic Block Store (EBS) is a managed block storage service that can be used to store data for EC2 instances.

Object Storage

- known for its scalability, cost efficiency, and suitability for static data and unstructured data
- Objects cannot be modified, meaning that data must be written entirely at once.
- Amazon Simple Storage Service (S3) is a managed object storage service that can be used to store and retrieve any amount of data from anywhere on the web.

## Database Storage

Relational Databases

- data stored in tables with rows and columns
- data is structured and can be queried using SQL
- key concepts:
  - Tables
  - Rows
  - Columns
  - Keys
  - Indexes
  - Constraints
  - Relationships
  - Views
  - Transactions

## Relational Database Concepts

- SQL
  - DML (Data Manipulation Language)
  - DDL (Data Definition Language)
  - DCL (Data Control Language)
  - TCL (Transaction Control Language)
- ACID Properties
  - Atomicity (all or nothing)
  - Consistency (data is always in a valid state)
  - Isolation (transactions are isolated from each other)
  - Durability (data is persistent)
- ER Model (Entity-Relationship Model)
  - Entity
  - Attribute
  - Relationship
  - Cardinality
  - Schema Normalization  -  process of organizing data in a database to reduce redundancy and improve data integrity by breaking up tables into smaller tables and defining relationships between them.
- Keys
  - Primary Key
  - Foreign Key
  - Composite Key
- Relational Database Management System Architecture
  - Query Processor
  - Query parser
  - Query optimizer
  - Execution plan
  - Execution engine
  - Storage engine
  - Buffer manager
  - Cache manager
  - Transaction manager
  - Concurrency control manager
  - Recovery manager
  - Security manager
  - Catalog
- Optimizing Relational Databases
  - Indexing - process of creating an index on a table
  - SQL tuning - process of optimizing SQL queries
  - Denormalization - process of adding redundant data to a database to improve read performance
  - Query federation - splitting a query into multiple queries that can be executed in parallel and then combining the results
- Scaling Relational Databases
  - Partitioning
    - dividing data into smaller manageable parts called partitions
    - each partition can be stored on a separate server
    - a record is stored in a partition based on a partition key and belongs to only one partition
    - Vertical partitioning - dividing a table into smaller tables with fewer columns
    - Horizontal partitioning - dividing a table into smaller tables with fewer rows
    - Hash partitioning - dividing data based on a hash function
    - Range partitioning - dividing data based on a range of values
  - Sharding
    - dividing data into smaller parts called shards
    - each shard can be stored on a separate server
    - a record is stored in a shard based on a shard key and belongs to only one shard
    - vertical sharding
    - horizontal sharding
    - elimindates central master server

  - Replication
    - process of copying data from one server to another
    - benefits:
      - high availability
      - load balancing
      - reduced latency
      - disaster recovery
      - scalability and performance
    - types of replication:
      - single-leader replication
      - multi-leader replication

- Open source relational databases
  - MySQL
  - PostgreSQL
