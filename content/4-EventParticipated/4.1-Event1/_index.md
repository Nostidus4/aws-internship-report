---
title: "Event 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy it verbatim** into your report, including this warning.
{{% /notice %}}

# Summary Report: “GenAI-powered App-DB Modernization workshop”

### Event Objectives

- Share best practices in modern application design
- Introduce Domain-Driven Design (DDD) and event-driven architecture
- Provide guidance on selecting the right compute services
- Present AI tools to support the development lifecycle

### Speakers

- **Jignesh Shah** – Director, Open Source Databases
- **Erica Liu** – Sr. GTM Specialist, AppMod
- **Fabrianne Effendi** – Assc. Specialist SA, Serverless Amazon Web Services

### Key Highlights

#### Drawbacks of legacy application architecture

- Long product release cycles → lost revenue and missed opportunities
- Inefficient operations → reduced productivity, higher costs
- Non-compliance with security regulations → security breaches, loss of reputation

#### Transitioning to microservices

Migrating to a modular system — each function is an **independent service** communicating via **events**, built on three core pillars:

- **Queue Management**: handle asynchronous tasks
- **Caching Strategy**: optimize performance
- **Message Handling**: flexible inter-service communication

#### Domain-Driven Design (DDD)

- **Four-step method**: identify domain events → arrange timeline → identify actors → define bounded contexts
- **Bookstore case study**: demonstrates real-world DDD application
- **Context mapping**: 7 patterns for integrating bounded contexts

#### Event-driven architecture

- **3 integration patterns**: publish/subscribe, point-to-point, streaming
- **Benefits**: loose coupling, scalability, resilience
- **Sync vs. async**: understanding the trade-offs

#### Compute evolution

- **Shared responsibility spectrum**: EC2 → ECS → Fargate → Lambda
- **Serverless benefits**: no server management, auto-scaling, pay-for-value
- **Functions vs. containers**: criteria for the appropriate choice

#### Amazon Q Developer

- **SDLC automation**: from planning to maintenance
- **Code transformation**: Java upgrade, .NET modernization
- **AWS Transform agents**: VMware, mainframe, and .NET migration

### Key Takeaways

- **Business-first design**: start from the business domain and a shared vocabulary (ubiquitous language) between business and tech teams, not from the technology itself.
- **Event storming**: a practical technique for modeling business processes into domain events, then splitting them into microservices with clear bounded contexts.
- **Event-driven over synchronous**: prefer async, event-driven communication for loose coupling, scalability, and resilience; know when to use pub/sub, point-to-point, or streaming.
- **Right-sized compute**: choose along the VM → container → serverless spectrum based on the workload, not by default.
- **Modernize in phases**: follow the 7Rs framework with a clear roadmap and measurable ROI — a full rewrite in one shot is risky.

### Applying to Work

- **Apply DDD** to current projects: run event storming sessions with business teams
- **Refactor microservices**: use bounded contexts to define service boundaries
- **Adopt event-driven patterns**: replace some synchronous calls with async messaging
- **Pilot serverless**: try AWS Lambda for suitable use cases
- **Try Amazon Q Developer**: integrate it into the dev workflow to boost productivity

### Personal Reflection

Attending the **“GenAI-powered App-DB Modernization”** workshop gave me a much clearer picture of how legacy systems are actually modernized in practice, beyond what I had read online. Hearing AWS specialists walk through real case studies — rather than just slides — made concepts like DDD and event-driven architecture click in a way that theory alone hadn't.

The most useful part was the event storming exercise: seeing a business process broken down into domain events step by step made bounded contexts feel like a concrete design tool rather than an abstract term. I also came away with a better sense of when *not* to reach for microservices or serverless — the speakers were clear that these are trade-offs, not universal upgrades.

I plan to bring the business-first mindset and the habit of questioning "sync or async, and why" into my own project work going forward.

#### Some event photos
*Add your event photos here*
