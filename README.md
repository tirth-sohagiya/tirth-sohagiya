# Tirth Sohagiya

Backend engineer, mostly Java and Spring Boot. I like the problems that show up when a system
gets busy and still has to give the right answer.

MS in Computer Science from Santa Clara University. Before that I spent about a year and a half
building Spring services on an IoT platform at Enlighted.

### Things I've built

**[ShelfLife](https://github.com/tirth-sohagiya/ShelfLife)** — Three Spring Boot services that
match surplus food donations to shelter requests, talking to each other only through Kafka
events. Saga orchestration releases reserved inventory when a pickup deadline lapses, and FEFO
allocation uses consistent lock ordering so concurrent requests can't deadlock. Tested against
real Postgres with Testcontainers, load tested with k6.

**[Balanced](https://github.com/tirth-sohagiya/Balanced)** — A double-entry ledger where every
transaction's journal entries must sum to zero before it saves, and balances are derived from
the entry log instead of stored. Twenty concurrent requests sharing one idempotency key produce
exactly one transaction.

**[Daily Digest](https://github.com/tirth-sohagiya/Daily-Digest)** — A serverless pipeline on
AWS that pulls nine public APIs into one daily email. 18 resources defined in Terraform, runs at
$0.00/month, and alarms on the absence of a successful run rather than only on errors.

### Tech

Java · Spring Boot · Apache Kafka · PostgreSQL · AWS (Lambda, DynamoDB, SES, EventBridge,
CloudWatch) · Terraform · Docker · Testcontainers · k6

---

Currently looking for backend roles.
[LinkedIn](https://www.linkedin.com/in/tirth-sohagiya) · tsohagiya007@gmail.com
