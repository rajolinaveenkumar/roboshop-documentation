### 🗃️ MongoDB (NoSQL)
```
Uses Collections and Documents (like JSON)
Flexible schema, good for unstructured or semi-structured data
```

### SQL Databases (e.g., MySQL, PostgreSQL)
```
Uses Tables and Rows
Rigid schema, great for structured data with strong relationships
```

### Redis (In-Memory Cache Database)

Acts as a CacheDB to speed up frequent queries
Typical flow:
```
App → Redis (Check if data exists)
     → If cache miss → DB
     → Save DB result into Redis (cache)
```
DB Flow without cache:
1.Open DB connection
2.Run query, get results
3.Close DB connection

### Messaging Queues
RabbitMQ, Kafka, ActiveMQ, JBoss ESB Server

Used for asynchronous communication

🔁 Communication Patterns
------------------------------------------------------------------------------------------------
*Synchronous

Sender expects an immediate response

Example: HTTP request

System-1 → HTTP → System-2 (must be online)
--------------------------------------------------------------------------------------------------------
*Asynchronous

Sender sends a message and doesn't wait for a response

Receiver can process it later

System-1 → MQ → System-2 (System-2 can be down)

Example: WhatsApp, YouTube Notifications
------------------------------------------------------------------------------------------------------------
