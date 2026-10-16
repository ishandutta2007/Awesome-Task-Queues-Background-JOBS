# Awesome-Task-Queues-Background-JOBS

# Awesome-Task-Queues-Background-JOBS

## Top Task Queues & Background Jobs Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Durable Workflows, Distributed Task Processing & Background Job Orchestration*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Task Queues & Background Jobs**. These tools let applications offload work to run asynchronously — sending emails, processing images, syncing data, running scheduled reports — without blocking the user or losing jobs when processes crash.

**Examples** include AWS SQS, Google Cloud Pub/Sub, Azure Service Bus, RabbitMQ, Temporal, Inngest, QStash, Celery, Sidekiq, and BullMQ (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, durable execution, and transparent task processing — ideal for developers prioritizing data sovereignty, avoiding per-message cloud costs, and maintaining full control over their job infrastructure.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[AWS SQS](https://aws.amazon.com/sqs/)**  
  Fully managed message queuing with Standard and FIFO queues. Standard queues offer at-least-once delivery and 99.999999999% durability across 3 AZs. FIFO queues provide exactly-once processing with 5-minute deduplication windows and per-message-group ordering. ~$12/month for 1M messages/day on Standard; FIFO adds a surcharge. Dead-letter queues via MaxReceiveCount for poison message handling. No message backup — consume and persist is the only durability strategy.

- **[Google Cloud Pub/Sub](https://cloud.google.com/pubsub)**  
  Fully managed, globally distributed messaging with automatic multi-zone replication. Simplest to operate — no shard or partition management. Supports ordering keys for per-group ordering and exactly-once delivery. ~$10/month for 1M messages/day. Push and pull delivery with schema validation (Avro, Protocol Buffers). 99.95% SLA.

- **[Azure Service Bus](https://azure.microsoft.com/en-us/products/service-bus/)**  
  Enterprise messaging with AMQP 1.0, sessions for ordered delivery, and transactions. **Richest enterprise feature set** — duplicate detection, SQL filters, correlation filters, and zone-redundant Premium tier. Standard tier is ~$10/month for 1M messages/day; Premium starts at ~$700/month for 1MU with advanced features. Lock duration 5s–5min (renewable) for visibility timeout.

- **[Temporal Cloud](https://temporal.io/)**  
  Managed durable execution platform for orchestrating long-running workflows with human-in-the-loop steps. The commercial service for the open-source Temporal engine, offering hosted scalability and support without running your own cluster.

- **[Inngest Cloud](https://www.inngest.com/)**  
  Managed event-driven workflow engine with durable functions and step functions. The commercial tier for the open-source Inngest project.

- **[QStash (Upstash)](https://upstash.com/docs/qstash)**  
  Serverless message queue and scheduler with **HTTP-based delivery** — send a message to any endpoint without managing infrastructure. **Free tier: 1,000 messages/day**. Pay-as-you-go: **$1 per 100K messages** with **retries free**. Fixed plans: **$180/month for 1M messages/day** or **$420/month for 10M messages/day**. **Prod Pack ($200/month)** adds uptime SLA, Prometheus, and Datadog integration. Max delay up to 1 year on paid tiers.

## Open-Source GitHub Projects

- **[Sidekiq](https://github.com/sidekiq/sidekiq)**  
  **The de facto background-job framework for Ruby and Rails.** Thread-based, Redis-backed, and memory-efficient with high throughput. Simple, reliable, and well-documented — the standard for Rails applications. **Open-source core is free (LGPL).** **Sidekiq Pro ($99/month)** adds reliable fetch, batches, and Pro metrics. **Sidekiq Enterprise (from $269/month)** adds unique jobs, rate limiting, and periodic jobs. Appliance licenses for distribution: **$14,995/yr (Pro)** and **$39,995/yr (Enterprise)**. Commercial support provides upgrade paths and bug fixes that open-source forks often lack.

- **[Celery](https://github.com/celery/celery)**  
  **The standard distributed task queue for Python.** BSD-3-Clause licensed — **no commercial plans, no hosted service, no billing relationship**. Runs on your own infrastructure with brokers including RabbitMQ, Redis, and Amazon SQS. Handles millions of tasks with retries, scheduling, and result backends. The foundation for Django, Flask, and FastAPI background processing.

- **[BullMQ](https://github.com/taskforcesh/bullmq)**  
  **Fast and robust queue system for Node.js built on Redis.** Carefully written for rock-solid stability and atomicity. Features **minimal CPU usage due to polling-free design**, distributed job execution, LIFO and FIFO, priorities, delayed jobs, scheduled/repeatable jobs, retries, concurrency settings per worker, and automatic crash recovery. 7.8K+ GitHub stars. Idempotency via custom `jobId` — BullMQ rejects IDs containing `:` so use safe delimiters or stable hashes. Defaults: 3 attempts, exponential backoff from 1 second.

- **[RabbitMQ](https://github.com/rabbitmq/rabbitmq-server)**  
  **The most mature open-source message broker** — Mozilla Public License 2.0. Supports **AMQP 1.0, MQTT 5.0, and STOMP** with no vendor lock-in. Routing, filtering, streaming, federation, and shovels for chaining deployments across environments. **Acknowledge message delivery and cluster replication** for durability. Used by millions worldwide with a vibrant global community. Commercial Tanzu RabbitMQ and Kubernetes operators available.

- **[Nuvom](https://github.com/nahom-zewdu/Nuvom)**  
  **Lightweight, plugin-first task queue for Python with no Redis or broker required.** **Windows-native** — no Linux-only assumptions. Static task discovery via **AST parsing** with zero import side-effects and manifest caching for fast CLI performance. Features retries with configurable delays, timeouts, result storage, and a Prometheus plugin exposing queue size, in-flight jobs, and worker count. Apache 2.0 licensed. Best for developers wanting Celery-style task queues without infrastructure dependencies.

- **[Quebec](https://pypi.org/project/quebec/)**  
  **PostgreSQL-backed task queue for Python** — no Redis or broker needed. Features **automatic job discovery** via `qc.discover_jobs("app.jobs")` recursively scanning packages. Delayed jobs with `wait` and `wait_until`, priority queues, automatic retries with configurable strategies, and a **web dashboard** via `control_plane='127.0.0.1:5006'`. Multiple queue support and per-instance job registration. Best for Python projects already using PostgreSQL that want a persistent, database-native task queue.

- **[Laravel Workflow](https://github.com/laravel-workflow/laravel-workflow)**  
  **Durable workflow engine for PHP powered by Laravel Queues** — inspired by Temporal and Azure Durable Functions. Allows tracking job status, orchestrating microservices, and writing long-running persistent distributed workflows. Best for Laravel teams wanting workflow orchestration without adopting a separate platform.

### Additional Strong Open-Source Options

- **Temporal (self-hosted)** — MIT-licensed durable execution engine. Run your own cluster for workflow orchestration with 6,700+ GitHub stars.
- **Inngest (self-hosted)** — Open-source event-driven workflow engine with durable functions. The open-source core for the managed service.
- **Dramatiq** — Fast, reliable Python task processing library. Redis and RabbitMQ backends.
- **RQ (Redis Queue)** — Simple Python job queue built on Redis. Lightweight and easy to understand.
- **Celery Beat** — Scheduler component of Celery for periodic task execution.

**Frameworks for building custom systems**: Combine **RabbitMQ** for protocol-agnostic, self-hosted message brokering, **Sidekiq** for Rails background jobs with commercial reliability tiers, **BullMQ** for Node.js with Redis, **Celery** or **Nuvom** for Python task processing, and **Temporal** for durable workflow orchestration — to build a complete self-hosted task queue ecosystem tailored to your stack.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Task queues and background job frameworks differ significantly in language support, broker requirements, and durability guarantees. **Sidekiq Pro/Enterprise provide commercial support and upgrade paths that open-source forks lack** — evaluate build-vs-buy based on operational risk. **Cloud queues (SQS, Pub/Sub, Service Bus) offer different ordering and exactly-once semantics** — SQS FIFO provides exactly-once within 5-minute windows, Pub/Sub with ordering keys, and Service Bus with sessions. **Retries are not idempotent by default** — your job handlers must be written to handle duplicate execution safely.
- Self-hosted open-source solutions require proper Redis/PostgreSQL/RabbitMQ infrastructure management, monitoring, and backup strategies.

---

**Made for backend engineers, platform teams, and developers building reliable asynchronous systems.**  
Let's make background job processing more open, resilient, and production-ready.
