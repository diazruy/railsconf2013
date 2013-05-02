# Data Storage

## Major players

### Mongo
- Tree structure, documents similar to JSON

### Redis
- In memory key-value store. Can persist to disk

### Cassandra
- Column family
- Data stored differently on disk than relational dbs
- Relational db is innefficient with sparse data

### Hbase
- column based
- hashmap

### CouchDB
- Document DB stored as JSON

### MarkLogic
- documents. stores in XML

### Neo4j
- graph database. easier to navigate hierarchical data

### riak
- distributed key-value store
- no intrinsic knowledge of data type stored

### couchbase
- in memory key-value store

## Some new players

### Titan
- distributed. graph db.

### existDB

### Datomic
-
## Why NoSQL?
- Fault tolerance - optimistic view that bad stuff is going to happen
  - distribution
  - routing
- High availability
  - parallelism
  - if losing partial connectivity to part of the distributed network, you can
    still send/receive from the visible part
- Consistency
- Scale
  - Axes
    - Throughput
    - Storage
    - Latency
  - Vertical - larger iron
  - Horizontal - more machines

Still no answer as to which NpSQL db to choose for a particular application

## Access Patterns
- Scheduled vs Spontaneous
  - Static vs Dynamic - any
  - Static/scheduled
  - Dynamic/scheduled - map reduce
  - Dynamic/spontaneous - most are not that great here

- Convert a dynamic static pattern into a static one if possible (?)

## Hybrid solutions
- Postgres for metadata, fetch key, use key to retrieve from Riak

