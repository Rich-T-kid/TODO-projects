# TODO-projects fall semester

## (1) Build SQLite (Similar)

Mini Projects (day-long, gist of the concept):
Buffer pool, Join, B+ Tree, Skip list, K-way external merge, SQL parser, Logical planner, Logical-to-physical planner, Write-ahead log

Database Query Optimizer Playground (capstone project):

Browser or mobile app frontend to visualize query plans

Backend in Go/Rust to:

Parse SQL

Convert to logical plan

Apply cost-based and rule-based optimizations

## (1.5) Custom In-Memory SQL Query Engine

**What:** Build an in-memory columnar cache that parses basic SQL (SELECT, WHERE, GROUP BY), converts to AST → logical plan → physical plan, and executes column-by-column with vectorized operators (scan, filter, projection, aggregate).

**Why:** Combines two critical database concepts—SQL query planning and columnar execution—showing how modern analytics engines like Trino/Arrow work under the hood.

**Takeaways:**
- Parse SQL into AST and map to relational algebra operators
- Execute queries column-by-column for cache efficiency and vectorization
- Understand why "batch-at-a-time" beats "row-at-a-time" processing
- Learn transformation rules (predicate pushdown, join reordering)
- Appreciate Arrow's memory model and SIMD optimization opportunities

## 2. Distributed Cache -> (https://github.com/Rich-T-kid/RapidStore)
In-memory cache cluster with eviction policies (LRU/LFU).

Support replication + consistent hashing.
Expose gRPC/HTTP APIs.

## 3. ~~Distributed Notes/Docs System~~ (Google Docs–lite) -> (https://github.com/Rich-T-kid/Draftly)
Support concurrent edits with CRDTs or OT (operational transforms).

Store history in a log + snapshots.

# quicker projects that focus on learning

##  (11) ~~Reverse Proxy with Load Balancing~~ (Repo) -> (https://github.com/Rich-T-kid/PivotProxy)
* Implement a proxy server in Go/Rust.
* Support round-robin, least-connections, weighted load balancing.
* Add health checks + failover.

## (22) ~~Service Discovery + Registry Like Consul or etcd-lite~~ (Repo) -> (https://github.com/Rich-T-kid/RouteFinder)
* In a microservices architecture, services (auth, payments, notifications, etc.) run on many machines or containers.
* Containers often get dynamic IP addresses (e.g., in Kubernetes, AWS ECS, GCP Cloud Run).
* Hardcoding addresses (like http://10.0.0.5:8080) doesn’t work because machines can move, die, or scale up/down.

## 33. ~~Music Queue for Parties (Distributed Jukebox)~~ -> (https://github.com/Rich-T-kid/BeatBus)
Guests join via QR code, queue songs.

Backend prevents duplicates, handles voting to skip.

Store song metadata + votes in Redis/Postgres.

# Personal weekend projects

## 55. ~~HTTP Server Built on a Raw TCP Server~~ -> (https://github.com/Rich-T-kid/Custom-HTTP-Server)
* The TCP server listens for client connections, accepts raw byte streams, and then parses the HTTP request format (method, path, headers, and body).
* Strengthens skills in network programming, parsing protocols, and managing connections.

## 66. Custom Parquet reader
* Implement a parquet reader that takes in a parquet file and prints it out in a pretty format

## 77 Custom json validator and parser
* take in json and check that its valid
* parse the json and grab its values
* no built in json librarys

## 88 Very basic LSM tree implementation
* Implement and test LSM tree Implementation

