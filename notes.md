---
Title : Node-React-Microservices
---

01-fundamentals-ideas-around-microservices

Problems with microservices
-data management between services

Each service gets its own database
Services will never, ever reach into another services database

Database-Per-Service
-we want each service to run indepently of other services
-Databse schema/structure might change unexpectedly
-Some services might function more efficiently with different types of database's

Communication Strategies Between Services
1 Sync
2 Async

Sync
-----Upside-----
Conceptually easy to understand
Service D won't need a database
-----Downside-----
Introduces a dependency between services
if any inter-service request fails, the overall request fails
the entire request is only as fast as the slowest request
can easily introduce webs of requests

Async
----Upside-----
Service D has zero dependenices on other services
Service D will be extermely fast
----Downside----
Data duplication
Harder to understand
