# TODO-projects

MINI projects (day long, just get the gist of the concept)
* Build Buffer pool 
* Write a join 
* Implement a B+ Tree
* Implement a skip list
* Implement K-way external merge
* Write a sql parser
* Write a logical planner from an sql query
* Write a logical to physical planner
* Implement a Write ahead log
  

7. Database Query Optimizer Playground
* Browser or mobile app frontend to visualize query plans
* Backend in Go/Rust to:
    * Parse SQL
    * Convert to logical plan
    * Apply cost-based and rule-based optimizations
* Optional: Python notebooks to simulate queries with metrics
🧠 Shows deep DB internals knowledge 📂 Recruiters at infra/database companies will LOVE this

(8) Lecture Q&A System with Ranking
Live question posting + upvote/downvote (like Stack Overflow in class).

Needs real-time WebSockets and distributed storage.

Backend handles hot-spot traffic (everyone upvoting the same Q).
👉 Great to show scalability under bursty loads.

(9) Music Queue for Parties (Distributed Jukebox)
Guests join via QR code, queue songs.

Backend prevents duplicates, handles voting to skip.

Store song metadata + votes in Redis/Postgres.
👉 Fun live demo at student parties.




Later:

(5) Reverse Proxy with Load Balancing
Implement a proxy server in Go/Rust.

Support round-robin, least-connections, weighted load balancing.

Add health checks + failover.


14. Distributed Cache
In-memory cache cluster with eviction policies (LRU/LFU).

Support replication + consistent hashing.

Expose gRPC/HTTP APIs.

3. Distributed Notes/Docs System (Google Docs–lite)
Support concurrent edits with CRDTs or OT (operational transforms).

Store history in a log + snapshots.

Deploy across multiple nodes.
👉 Hits both databases + networking.

4. Live Network Latency Visualizer Across Multiple Locations
🧩 Like: a “PingMap” of server health
Features:
* Deploy ping agents to multiple cloud regions (EC2, fly.io, etc.)
* Central dashboard aggregates results
* Visualize latency and outages in a map or graph
* Optional: anomaly detection or alerting
Tech:
* Rust or Go agents
* Python FastAPI or Go backend
* Frontend: React/D3 or CLI (ASCII graphs)
Why it's 🔥:
* Distributed, real-world use case
* Gives you a strong visual demo
* Teaches you about real-world latency and reliability




Music Recommender from Lyrics + Tempo + Vibes
Scrape lyrics + audio metadata and build a hybrid content-based recommender.
* Use: Lyrics embedding (BERT) + tempo + mood metadata
* Build scoring function based on user listening habits
* Optional: audio fingerprinting or similarity graph
🧠 Learn: hybrid recommender systems, music ML, cosine similarity 💥 Fun and highly demoable
