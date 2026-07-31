---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 5 Objectives:

* Build REST APIs for the product catalog and for placing/tracking orders.
* Learn Spring Security to protect the seller portal (form login + CSRF).

### Tasks to be carried out this week:
| Day | Task                                                                                              | Start Date | Completion Date | Reference Material                        |
| --- | -------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| 2   | - Implemented `GET /api/products` and `GET /api/products/{id}` with DTO mapping                     | 09/08/2025 | 09/08/2025      |
| 3   | - Implemented `POST /api/orders` (COD/VietQR selection) and `GET /api/orders/{code}` for tracking   | 09/09/2025 | 09/09/2025      |
| 4   | - Learned Spring Security fundamentals: filter chain, authentication, authorization                 | 09/10/2025 | 09/10/2025      | <https://docs.spring.io/spring-security/reference/> |
| 5   | - Configured form login + CSRF protection for the `/seller/**` routes                                | 09/11/2025 | 09/11/2025      |
| 6   | - Wrote integration tests for product & order controllers using MockMvc                             | 09/12/2025 | 09/12/2025      |


### Week 5 Achievements:

* Core REST API functional end-to-end: catalog browsing, checkout (COD/VietQR), and order tracking by code.
* Seller portal routes protected by form-login authentication with CSRF enabled.
* Integration tests for the controller layer pass consistently in the local build.
* ...
