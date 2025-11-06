✅ Easy (5 Questions)

What is the difference between GET and POST HTTP methods?

What is a REST API? Explain it in simple terms.

What is CORS and why is it needed?

What is the purpose of an ORM (Object Relational Mapper) like Sequelize / Hibernate / Entity Framework?

What is the difference between synchronous and asynchronous programming?

🟡 Medium (15 Questions + Scenario-Based)

Explain MVC Architecture and why backend frameworks commonly use it.

What is JWT (JSON Web Token)? How does it help in authentication?

Scenario:
You have a login API. After entering the correct password, it still logs the user out after some time.
How would you implement refresh tokens to keep the user logged in?

What is connection pooling in databases and why is it necessary?

Explain indexing in SQL.
When would adding an index improve performance and when can it hurt?

Scenario:
A query is taking too long to execute in production.
How would you diagnose and optimize it?

What are WebSockets?
How are they different from HTTP polling or Server-Sent Events?

Explain the concept of Middleware in backend frameworks (Express / NestJS / Django / Laravel etc.).

What is rate limiting and how would you implement it to avoid abuse of your APIs?

Scenario:
You have an endpoint /get-user-details. It is being called thousands of times repeatedly with the same user ID.
Where would caching be appropriate and what tool would you use (Redis / In-Memory / CDN)?

What is SQL Injection?
Show one way to prevent it.

What is ACID in databases? Explain each term.

Difference between Monolithic and Microservice architecture?
When should you prefer one over the other?

Scenario:
Your microservices communicate over HTTP and response time is becoming slow.
What communication alternatives would you consider? (gRPC, Message Queue, Kafka, RabbitMQ, etc.)

What is a Reverse Proxy (e.g., Nginx)? How does it improve performance?

Explain the difference between vertical scaling and horizontal scaling.

Scenario:
You deployed backend updates but some users are still getting old results due to caching.
How will you handle cache invalidation?

🔥 Difficult (5 Questions)

Design a scalable notification delivery system (Email + WhatsApp + Push Notifications).
Explain architecture, queues, retries, and failure handling.

Explain CAP Theorem and where MongoDB and PostgreSQL fall in that model.

Given a microservices architecture with 20+ services, how will you implement:

Distributed Logging

Distributed Tracing

Centralized Monitoring
(Tools: ELK Stack, Jaeger, Prometheus, Grafana)

Scenario:
Your application is facing high write load on a single DB server.
How would you scale the database write operations?
Discuss: Sharding vs Replication vs Partitioning.

How would you design a rate limiter used globally across distributed servers?
Discuss token bucket, Redis atomic increments, and cluster synchronization.