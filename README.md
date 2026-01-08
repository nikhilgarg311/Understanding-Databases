# Understanding-Databases

### SQL vs NoSQL.

- SQL
    ACID properties
    Structured Data
    Dificult to scale( needs heavy infra)
    Efficient for complex queries and transactions
    example MySQL, Oracle, PostgreSQL
- NoSQL
    Unstructured data, document form.
    Easy to scale
    fast read/write for large scale data
    example MongoDb, Cassandra, CouchDB, Neo4j

---

### Why we need to scale databases?


---

### What are various strategies to scale databases?

- Indexing: Indexing means storing a cloumn in sorted manner in a different allocating a memory, with pointer to original row, so that binary search can be applied and things can searched in O(logn). B-trees, trees data structures are used. Read intensive tables should be indexed, because after create/update query trees will have to rebalance.

- Vertical Scaling: adding cpu, ram, storage. Limit to how much can be added. Single point of failure.

- Sharding: splitting larger datasets into smaller.

- Materialised views: precomputing complex queries, like daily report generation from large dataset.

- De-materialisec views: avoiding different tables to avoid complex joins.

- Caching: 

- Replication: create replicas of primary database on various servers to handle reads, increase availability and fault tolerance.