---
title: "Week 4 Worklog"
date: 2026-07-06
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Initialize the Shopsflow Backend project architecture (Spring Boot 4, Java 21) and set up the local development environment.
* Configure local PostgreSQL database and integrate Flyway for automated schema migrations.
* Draft the complete Proposal documentation (Section 2.3) for the team.

### Tasks to be implemented this week:

| Day | Tasks | Start Date | End Date |
| :---: | :--- | :---: | :---: |
| **Mon** | - Generate project skeleton via Spring Initializr, selecting Java 21, Spring Boot 4, and initial dependencies | 06/07/2026 | 06/07/2026 |
| **Tue** | - Configure `pom.xml`, install development tools, and set environment variables in `.env` (DB URL, Username, Password) | 07/07/2026 | 07/07/2026 |
| **Wed** | - Set up local PostgreSQL database and verify persistence connectivity via Spring Data JPA | 08/07/2026 | 08/07/2026 |
| **Thu** | - Integrate Flyway Migration, configure script paths, and write initial SQL migration file (`V1__init.sql`) | 09/07/2026 | 09/07/2026 |
| **Fri** | - Define core JPA Entities (`User`, `Product`, `Category`) and underlying Repository interfaces <br> - Draft Section 2.3 Proposal (Overview, architecture, timeline, budget) | 10/07/2026 | 10/07/2026 |

### Week 4 Achievements:

* Core Backend infrastructure set up successfully and running smoothly locally.
* Linked PostgreSQL database and automated schema migrations via Flyway.
* Built core JPA Entities representing the database structure of the Shopsflow application.
* Completed 100% of Section Proposal documentation for the Shopsflow system.