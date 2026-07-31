---
title: "Week 4 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 4 Objectives:

* Design the core domain model (Product, Category, Order, Customer) with Spring Data JPA.
* Continue building the schema through Flyway-managed migrations.

### Tasks to be carried out this week:
| Day | Task                                                                                                 | Start Date | Completion Date | Reference Material                        |
| --- | -------------------------------------------------------------------------------------------------------| ---------- | --------------- | ----------------------------------------- |
| 2   | - Modeled `Product`/`Category` entities with JPA annotations and relationships                          | 09/01/2025 | 09/01/2025      | <https://docs.spring.io/spring-data/jpa/reference/> |
| 3   | - Modeled `Order`/`OrderItem`/`Customer` entities <br> - Defined the order status enum (pending/paid/shipped/...) | 09/02/2025 | 09/02/2025      |
| 4   | - Wrote Flyway migrations for `orders` and `customers` tables <br> - Seeded sample data for local testing | 09/03/2025 | 09/03/2025      | <https://flywaydb.org/documentation/> |
| 5   | - Implemented Spring Data JPA repositories (`ProductRepository`, `OrderRepository`, ...)                | 09/04/2025 | 09/04/2025      |
| 6   | - Wrote repository unit tests against a Dockerized test PostgreSQL instance                             | 09/05/2025 | 09/05/2025      |


### Week 4 Achievements:

* Core schema (product, category, order, order item, customer) fully migrated via Flyway.
* All repositories covered by unit tests running against a real PostgreSQL container.
* Gained a solid understanding of JPA relationship mapping (`@OneToMany`/`@ManyToOne`) and cascade behavior.
* ...
