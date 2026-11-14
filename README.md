<h1 align="center">Hi, I'm Seif Arafaa 👋</h1>
<h3 align="center">Senior Backend Software Engineer · Berlin, Germany</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/seif-arafaa"><img src="https://img.shields.io/badge/LinkedIn-seif--arafaa-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:seifarafaa@gmail.com"><img src="https://img.shields.io/badge/Email-seifarafaa%40gmail.com-D14836?style=flat&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Location-Berlin%2C%20DE-2E7D32?style=flat&logo=googlemaps&logoColor=white" alt="Berlin">
</p>

I build **event-driven backend systems on the JVM** (Java, Spring Boot) and run them on **AWS** and **GCP**. I have 4+ years of experience across telecom, e-commerce and fintech. I like owning a system end to end, from the architecture to how it behaves in production, and I design around the failure cases first.

- 🏢 **Senior Backend Software Engineer at Etisalat (e&)**, working on the Twist platform: accounts, subscriptions, loyalty and commerce
- 🛒 Previously at **Wayfair** in Berlin, building order fulfillment services on GCP
- 🤖 **AI backend consultant for Finc Wealth**, a fintech building tools for asset managers on the Egyptian market
- 🎓 MSc in Computer Science, **German International University Berlin**, with a focus on machine learning and AI

---

## 🔧 What I've built

### At Etisalat (e&): Twist platform

| Project | What it does | Stack |
|---|---|---|
| **Subscription module** | I designed and led the new subscription module, which brings plans and purchase logic into one place. It has saved about **$8K** so far and grown active subscriptions by **10%**. I also fixed old entitlement bugs that left some accounts on premium through exploits, which closed a revenue leak. | Java, Spring Boot, AWS SQS |
| **Loyalty rewards engine** | A dynamic rewards and bonus engine for the loyalty service, covering achievements, wallets, packages and redemptions. It uses hexagonal architecture, and every reward step is driven by events. | Java 21, Spring WebFlux, DynamoDB, SQS |
| **Observability layer** | Real-time alerting plus a shared-kernel metrics library that streams custom performance metrics from internal and third-party services to CloudWatch. It cut the mean time to detect production incidents by **30–40%** across several backend teams. | Micrometer, AWS CloudWatch |
| **Twist Commerce** | I'm leading the design and build of a commerce backend for the Twist Games app, which sells digital products such as game vouchers and top-ups. It checks stock, supplier balance and budget before any charge, and its fulfillment workflows can roll back and recover from partial failures. | Medusa 2, Node.js, TypeScript, PostgreSQL |
| **API gateway proof of concept** | A benchmarked GraalVM native gateway in front of the account services. It adds about **0.5–2 ms at p50** and stays under **5 ms at p99**, starts in about 0.05 s, and failed 0% of requests under load. | Quarkus, GraalVM, k6 |
| **ClickStack observability proof of concept** | Checked that logs, traces and metrics all flow end to end from a Spring WebFlux service through OpenTelemetry into ClickHouse and HyperDX, with sensitive fields masked in the logs. | OpenTelemetry, ClickHouse, HyperDX |

On top of these, I reduced cloud infrastructure costs by **20–25%** across the account and loyalty microservices.

### For Finc Wealth: fintech

| Project | What it does | Stack |
|---|---|---|
| **FINC API** | The backend of a B2B investment platform for asset managers on the Egyptian Exchange (EGX). It handles trading, holdings, portfolio analytics and market data. An **append-only transaction ledger is the single source of truth**: holdings and balances are rebuilt by replaying it, edits create new revisions and nothing is ever deleted, so every balance and P&L figure reconciles exactly. It uses JWT auth, checks who owns each object, and returns errors in one consistent format. | Java 21, Spring Boot 3, Spring Security, PostgreSQL, MongoDB Atlas, Flyway, Heroku |
| **Fincr** | An LLM assistant that answers plain-English questions about the Egyptian stock market. A classifier sends each question either to a **RAG** pipeline (ChromaDB) or to a **natural-language-to-SQL** pipeline over DuckDB, which covers 259 tickers and 5 years of company financials. The generated SQL is checked and rewritten before it runs: it is limited to read-only SELECT queries, company names are resolved, and common questions use templates instead of the model. This keeps the model's unpredictable output safe to execute. | Python, FastAPI, Ollama, ChromaDB, DuckDB |

### At Wayfair

- **Same-day order processing.** I led the redesign of the fulfillment flow, which cut delivery time by **55–65%** (from 5–7 days to 2–3 days).
- Cloud-native microservices and REST APIs on GCP and PostgreSQL, handling millions of transactions a day, with full unit and integration test coverage.
- CI/CD with Buildkite, Kubernetes and Docker, and monitoring with Datadog, Elasticsearch and PagerDuty.

> Most of this work is proprietary, so the repositories are private. I'm happy to walk through the architecture and design decisions in a conversation.

---

## 🧰 Tech stack

**Languages**<br>
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)

**Frameworks**<br>
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat&logo=springsecurity&logoColor=white)
![Quarkus](https://img.shields.io/badge/Quarkus-4695EB?style=flat&logo=quarkus&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Medusa](https://img.shields.io/badge/Medusa-000000?style=flat&logo=medusa&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat&logo=graphql&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)

**Data and messaging**<br>
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![DynamoDB](https://img.shields.io/badge/DynamoDB-4053D6?style=flat&logo=amazondynamodb&logoColor=white)
![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=flat&logo=duckdb&logoColor=black)
![AWS SQS](https://img.shields.io/badge/AWS%20SQS-FF4F8B?style=flat&logo=amazonsqs&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat&logo=rabbitmq&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat&logo=elasticsearch&logoColor=white)

**Cloud and DevOps**<br>
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![GCP](https://img.shields.io/badge/Google%20Cloud-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Buildkite](https://img.shields.io/badge/Buildkite-14CC80?style=flat&logo=buildkite&logoColor=white)
![Heroku](https://img.shields.io/badge/Heroku-430098?style=flat&logo=heroku&logoColor=white)

**Observability**<br>
![CloudWatch](https://img.shields.io/badge/CloudWatch-FF4F8B?style=flat&logo=amazoncloudwatch&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat&logo=opentelemetry&logoColor=white)
![Datadog](https://img.shields.io/badge/Datadog-632CA6?style=flat&logo=datadog&logoColor=white)
![PagerDuty](https://img.shields.io/badge/PagerDuty-06AC38?style=flat&logo=pagerduty&logoColor=white)

**AI and LLMs**<br>
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6446?style=flat)
![RAG](https://img.shields.io/badge/RAG-NL--to--SQL-8A2BE2?style=flat)
![Claude Code](https://img.shields.io/badge/Claude%20Code-D97757?style=flat&logo=claude&logoColor=white)

---

## 🧭 How I work

- **Design for failure first.** Check before charging, make operations idempotent, roll back safely, and fail closed when unsure.
- **One source of truth.** I prefer append-only ledgers and events over state that gets updated in place.
- **Measure before deciding.** I write a proof of concept with benchmarks before adopting a new piece of infrastructure.
- **Clean architecture.** I apply hexagonal architecture, DDD and SOLID, and I write docs that a new teammate can actually follow.
- **AI-assisted, human-owned.** I use Claude Code every day, and I take full responsibility for every decision that ships.

---

<p align="center">
  🗣️ English (fluent) · German (B1)
</p>
