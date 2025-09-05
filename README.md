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


## 2. Distributed Notes/Docs System (Google Docs–lite)
Support concurrent edits with CRDTs or OT (operational transforms).

Store history in a log + snapshots.


## 3. Lecture Q&A System with Ranking
Live question posting + upvote/downvote (like Stack Overflow in class).

Needs real-time WebSockets and distributed storage.

Backend handles hot-spot traffic (everyone upvoting the same Q).
👉 Great to show scalability under bursty loads.



# quicker projects that focus on learning

##  (11) ~~Reverse Proxy with Load Balancing~~ (Repo) -> (https://github.com/Rich-T-kid/PivotProxy)
* Implement a proxy server in Go/Rust.
* Support round-robin, least-connections, weighted load balancing.
* Add health checks + failover.

## (22) Service Discovery + Registry Like Consul or etcd-lite. (Repo) -> (https://github.com/Rich-T-kid/RouteFinder)
* In a microservices architecture, services (auth, payments, notifications, etc.) run on many machines or containers.
* Containers often get dynamic IP addresses (e.g., in Kubernetes, AWS ECS, GCP Cloud Run).
* Hardcoding addresses (like http://10.0.0.5:8080) doesn’t work because machines can move, die, or scale up/down.

## 33. Music Queue for Parties (Distributed Jukebox)
Guests join via QR code, queue songs.

Backend prevents duplicates, handles voting to skip.

Store song metadata + votes in Redis/Postgres.

# Later down the line/ slighly more complex and time consuming
## (44) Distributed Cache
In-memory cache cluster with eviction policies (LRU/LFU).

Support replication + consistent hashing.
Expose gRPC/HTTP APIs.


# Personal weekend projects

## 55 Build your own grep (CodeCrafters);
* just follow it, seems pretty concise and straightforward compared to other projects on here

## 66. HTTP Server Built on a Raw TCP Server
* The TCP server listens for client connections, accepts raw byte streams, and then parses the HTTP request format (method, path, headers, and body).
* Strengthens skills in network programming, parsing protocols, and managing connections.


## 77 Implement Redis (CodeCrafters): build a Redis-compatible server from scratch—RESP parser, 
* PING/ECHO/SET/GET/DEL/INCR, key expirations (EX/PEX), pipelining, basic transactions (MULTI/EXEC),
*  persistence (RDB snapshot + AOF), simple replication (REPLCONF/PSYNC), optional LRU eviction;
*  enchmark with redis-benchmark, containerize, and add C

