# Tirth Sohagiya

**Backend Engineer | Java · Spring Boot · Distributed Systems · AWS**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tirth-sohagiya)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tsohagiya007@gmail.com)

---

### About

I build backend systems in Java and Spring Boot. Most of what I find interesting is what happens
when a system gets busy and still has to give the right answer: two requests racing for the same
row, a service dying halfway through a transaction, a retry that shouldn't double-charge someone.

MS in Computer Science from Santa Clara University. Before that I spent about a year and a half
at Enlighted building Spring services on an IoT platform running 50,000+ connected devices.

Currently looking for backend roles.

---

### Tech

<p>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg" width="42" height="42" alt="Java"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/spring/spring-original.svg" width="42" height="42" alt="Spring"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/apachekafka/apachekafka-original.svg" width="42" height="42" alt="Kafka"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg" width="42" height="42" alt="PostgreSQL"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mysql/mysql-original.svg" width="42" height="42" alt="MySQL"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mongodb/mongodb-original.svg" width="42" height="42" alt="MongoDB"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/redis/redis-original.svg" width="42" height="42" alt="Redis"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/amazonwebservices/amazonwebservices-plain-wordmark.svg" width="42" height="42" alt="AWS"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/terraform/terraform-original.svg" width="42" height="42" alt="Terraform"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original.svg" width="42" height="42" alt="Docker"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" width="42" height="42" alt="Python"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" width="42" height="42" alt="Git"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/linux/linux-original.svg" width="42" height="42" alt="Linux"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/intellij/intellij-original.svg" width="42" height="42" alt="IntelliJ"/>
</p>

Also: Hibernate · Spring Security · REST / SOAP · Testcontainers · k6 · JUnit · Mockito · GitHub Actions

---

### Projects

**[ShelfLife](https://github.com/tirth-sohagiya/ShelfLife)** · Java, Spring Boot, Kafka, PostgreSQL, Docker

Three microservices matching surplus food donations to shelter requests, each owning its own
database and communicating only through Kafka events. A saga layer releases reserved inventory
when a pickup deadline lapses, and FEFO allocation uses consistent lock ordering so concurrent
requests can't deadlock.

Verified with 37 tests against real PostgreSQL via Testcontainers, including a concurrency test
that allocated **1,000/1,000 units with zero oversell across 100 simultaneous threads**. Load
tested end to end with k6 at **p95 under 200 ms, 0% failure rate**.

**[Balanced](https://github.com/tirth-sohagiya/Balanced)** · Java, Spring Boot, PostgreSQL, Spring Security, k6

A double-entry ledger where every transaction's journal entries must sum to zero before it
persists, and account balances are derived from the entry log rather than stored as mutable
state. Idempotency comes from a composite (user, key) constraint plus a dedicated transactional
write boundary.

**20 concurrent requests sharing one idempotency key produce exactly one transaction.** API
sustained ~133 req/s at p99 32.88 ms with a 0% error rate.

**[Daily Digest](https://github.com/tirth-sohagiya/Daily-Digest)** · Java, AWS Lambda, Terraform, DynamoDB, SES

A scheduled serverless pipeline that pulls nine public APIs into one daily email, provisioned as
**18 AWS resources in Terraform**. Every source sits behind a one-method interface and is invoked
in isolation, so a failing provider costs one section rather than the whole run.

Runs at **$0.00/month** after replacing a $0.01-per-request Cost Explorer call with a free
CloudWatch metric. Stream-parses a 13 MB, 19,000-record JSON feed one element at a time, holding
peak memory to **213 MB of a 512 MB allocation**. Alarms on the absence of a successful run in
36 hours, not only on errors.

---

### Experience

**Software Development Engineer** · Enlighted Inc. · Oct 2022 – Feb 2024

Built Spring services on an IoT platform serving 50,000+ connected devices. Integrated 12+
REST and SOAP interfaces with Jersey and Apache Axis. Cut average API response time from
650 ms to 468 ms by eliminating redundant queries and excessive Hibernate entity loading.

**Software Engineering Intern** · Hidden Brains InfoTech · Aug 2020 – Mar 2021

Java/J2EE backend modules, JMS publish-subscribe messaging with Tibco EMS, SOAP web services
via SAAJ.

---

### Education

**MS, Computer Science and Engineering** · Santa Clara University · 2026 · With Distinction
**BS, Computer Science** · San Jose State University · 2022 · Cum Laude
