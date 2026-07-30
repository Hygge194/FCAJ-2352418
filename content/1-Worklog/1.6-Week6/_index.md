---
title: "Week 6 Worklog"
date: 2026-07-20
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Develop Shopping Cart and Order APIs, completing the core checkout workflow.
* Handle inventory race conditions under concurrent purchasing (Concurrency Control).
* Develop Product Review APIs and write business logic Unit Tests.

### Tasks to be implemented this week:

| Day | Tasks | Start Date | End Date |
| :---: | :--- | :---: | :---: |
| **Mon** | - Develop Shopping Cart APIs (Cart Controller & Service) managing items addition, quantity updates, and removal | 20/07/2026 | 20/07/2026 |
| **Tue** | - Develop Order APIs (Order Controller & Service), converting active Cart into `PENDING` Order status | 21/07/2026 | 21/07/2026 |
| **Wed** | - Implement Optimistic Locking using `@Version` field on Product entity to control stock concurrency | 22/07/2026 | 22/07/2026 |
| **Thu** | - Build Product Review APIs (permitting verified purchasers to review, and authors to edit/delete their own reviews) | 23/07/2026 | 23/07/2026 |
| **Fri** | - Write Mockito Unit Tests for core Services (`CartService`, `OrderService`, `ProductService`) verifying business logic correctness | 24/07/2026 | 24/07/2026 |

### Week 6 Achievements:

* Completed seamless Cart management and Order Checkout workflow.
* Resolved Over-selling concurrency issues using Optimistic Locking.
* Product Review APIs and core backend service Unit Tests implemented with high test coverage.