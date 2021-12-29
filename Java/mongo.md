# Mongo DB

(from 视频课)

* NoSQL
  * Key-value: Redis
  * column-based: Hbase, Cassandra
  * Document: Mongo, CouchDB
  * Graph DB: Neo4J

---

* Hierarchy in Mongo
  * Database
  * Collection
  * Document
  * Field

## CRUD

[doc](https://docs.mongodb.com/manual/crud/)

## Aggregation

[doc](https://docs.mongodb.com/manual/aggregation/)

* Pipeline
* Map-reduce

## Index

[doc](https://docs.mongodb.com/manual/indexes/)

## Replication

[doc](https://docs.mongodb.com/manual/replication/)

primary-secondary

* 1 primary node
* multiple secondary nodes

priority

* standard node
  * (standard) `"priority"` > 0
* passive, not a candidate of primary node, only serve as secondary node
  * `"priority": 0`
* (optional) arbiter, participates in elections but does not hold data
  * `"arbiterOnly": true`

## Sharding

[doc](https://docs.mongodb.com/manual/sharding/)

* routers, 1 or more
* config servers (1 replica set)
* multiple shard (each is a replica set)
