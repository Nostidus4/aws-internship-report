---
title: "Week 7 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.7. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 7 Objectives:

* Build the product catalog, cart, and checkout pages.
* Integrate the frontend with the backend REST APIs and bundle it into the Spring Boot `static/` folder.

### Tasks to be carried out this week:
| Day | Task                                                                                             | Start Date | Completion Date | Reference Material                        |
| --- | ----------------------------------------------------------------------------------------------------| ---------- | --------------- | ----------------------------------------- |
| 2   | - Built the Product listing & detail pages <br> - Wrote a typed API client (fetch + TS interfaces)  | 09/22/2025 | 09/22/2025      |
| 3   | - Built the Cart page (local state) and the Checkout form (COD/VietQR)                              | 09/23/2025 | 09/23/2025      |
| 4   | - Built the Order Tracking page (lookup by order code)                                              | 09/24/2025 | 09/24/2025      |
| 5   | - Configured the Vite build to output into `src/main/resources/static` (same-origin, no CORS)       | 09/25/2025 | 09/25/2025      | <https://vitejs.dev/config/build-options.html> |
| 6   | - Built the Seller Dashboard skeleton (product & order management UI)                               | 09/26/2025 | 09/26/2025      |


### Week 7 Achievements:

* Full customer-facing flow working locally end-to-end: browse → cart → checkout → track order.
* Frontend build bundled directly into the Spring Boot jar, running same-origin with no CORS configuration needed.
* Seller Dashboard skeleton ready for wiring up to the product/order management APIs.
* ...
