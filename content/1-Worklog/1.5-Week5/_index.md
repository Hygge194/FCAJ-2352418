---
title: "Week 5 Worklog"
date: 2026-07-13
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Implement Spring Security authentication mechanisms integrated with Stateless JWT Tokens.
* Develop Category APIs and Product APIs enforcing Role-based Access Control.

### Tasks to be implemented this week:

| Day | Tasks | Start Date | End Date |
| :---: | :--- | :---: | :---: |
| **Mon** | - Configure Spring Security, build `JwtUtil` for token generation during login and token parsing during requests | 13/07/2026 | 13/07/2026 |
| **Tue** | - Develop Registration and Login APIs (`/api/auth/register`, `/api/auth/login`), hashing passwords using BCrypt | 14/07/2026 | 14/07/2026 |
| **Wed** | - Implement `JwtFilter` filter and endpoint security rules (only `ADMIN` role permitted to create/update/delete products/categories) | 15/07/2026 | 15/07/2026 |
| **Thu** | - Build CRUD APIs for Category and Product, implementing search filters by category, price range, and keywords | 16/07/2026 | 16/07/2026 |
| **Fri** | - Configure `GlobalExceptionHandler` for central error handling and integrate `springdoc-openapi` for Swagger UI testing | 17/07/2026 | 17/07/2026 |

### Week 5 Achievements:

* JWT authentication system functioning accurately and securely.
* Completed CRUD APIs for Products and Categories with strict role-based access control.
* Integrated Swagger UI at `/swagger-ui.html` facilitating smoother frontend-backend API testing.