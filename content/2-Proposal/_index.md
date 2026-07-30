---
title: "Proposal"
date: 2026-06-15
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

In this section, I would like to summarize the proposed contents for my internship project: **Shopsflow Backend**.

# Shopsflow Backend
## A Comprehensive and Secure E-commerce Platform Deployed on AWS

### 1. Executive Summary
**Shopsflow** is an e-commerce platform project designed to provide a smooth and secure online shopping experience. Within the scope of this internship, the project focuses on building a robust **Backend** system using Java Spring Boot, integrating cart management, resolving database concurrency/inventory conflicts during high-traffic checkouts, and facilitating online payments via the VNPay sandbox gateway. The entire system is designed for deployment on AWS cloud infrastructure to ensure high availability, security, and easy scalability.

### 2. Problem Statement
**Current Problems**
Small-scale online retail systems often struggle to manage inventory records during sudden traffic spikes, leading to over-selling issues. Furthermore, integrating secure domestic payment gateways (preventing webhook IPN tampering and credential leaks) and securing user APIs remain significant technical challenges.

**The Solution**
Shopsflow Backend leverages:
*   **Java 21 & Spring Boot 4**: Builds fast, compliant, and standard RESTful APIs.
*   **Spring Security & JWT**: Manages stateless authentication and role-based access control (RBAC).
*   **Optimistic Locking**: Fully resolves inventory concurrency issues.
*   **VNPay Integration**: Processes secure payments using SHA512 signature validation.
*   **AWS Services**: Deployed on Amazon EC2, using Amazon RDS (PostgreSQL) for the database to ensure transactional stability, and Amazon S3 for storing static assets (product images).

**Benefits and Return on Investment (ROI)**
The solution provides a complete backend framework ready to integrate with any Frontend platform (Web/App). By adopting AWS managed services like RDS, the system eliminates manual database patching and maintenance overhead, allowing developers to focus on feature delivery.

### 3. Solution Architecture

![Architecture Diagram](/images/5-Workshop/5.1-Workshop-overview/diagram1.jpg)

**Core AWS Services Used**
- **Amazon VPC**: Establishes isolated subnets (Public/Private) to secure the database.
- **Amazon EC2**: Hosts the Spring Boot application.
- **Amazon RDS (PostgreSQL)**: Serves as the relational database managing User, Product, and Order tables.
- **Amazon S3**: Stores static product images.
- **AWS IAM**: Manages secure resource access policies.

**Component Design**
- **Security Module**: JWT Authentication & Role-based Access Control.
- **Catalog Module**: Categories and products CRUD management.
- **Checkout Module**: Cart, Orders, and inventory management using Optimistic Locking.
- **Payment Module**: VNPay checkout flow and IPN Webhook processing.

### 4. Technical Implementation
**Phases of Implementation**
The project spans 4 main phases over 9 weeks:
1. **Architecture & Setup**: Designing the database schema, setting up development environments, and configuring AWS VPC network topology.
2. **Core API Development**: Implementing JWT authentication, and Product/Category CRUD operations.
3. **Checkout Flow**: Building cart and order endpoints, and applying Optimistic Locking to prevent over-selling.
4. **Payment & Cloud Integration**: Integrating VNPay Sandbox, writing Unit Tests, and deploying backend applications to EC2 and RDS.

**Technical Requirements**
- Backend: Java 21, Spring Boot, Maven, Flyway (Migration).
- Database: PostgreSQL.
- Cloud: AWS CLI, SSH (EC2), Security Groups configurations.

### 5. Roadmap & Key Milestones
- **Month 1 (Weeks 1-4)**: AWS training, database design, Spring Boot project initialization, and Proposal submission.
- **Month 2 (Weeks 5-9)**: API development (Cart, Order, Payment), Concurrency handling, Unit Tests, Blog documentation, and Final Project packaging.

### 6. Budget Estimation
*Estimated monthly AWS charges for the Dev/Test environment (maximizing Free Tier limits):*
- **Amazon EC2 (t3.micro)**: Free-tier eligible, or ~8-10 USD/month.
- **Amazon RDS (db.t3.micro)**: Free-tier eligible, or ~15 USD/month.
- **Amazon S3**: Minimal storage, costs < 0.1 USD/month.
- **Data Transfer**: Free under 100GB.
*=> Total reference cost: ~20-25 USD/month if Free Tier is expired.*

### 7. Risk Assessment
**Risk Matrix**
- Database credentials/Secret Key leak: High impact, Low probability.
- VNPay payment logic loophole/tampering: High impact, Medium probability.
- AWS Free-tier expiration: Medium impact.

**Mitigation Strategies**
- Never commit credentials to GitHub; use Parameter Store or Environment Variables.
- Write rigorous unit tests (`VnPayServiceTest`) and secure request logging.
- Set up **AWS Budgets** to trigger email alarms if charges exceed $1.

### 8. Expected Outcomes
- A complete backend API capable of handling checkouts and VNPay payments.
- Secure frontend-backend communication.
- Enhanced Java coding, AWS Cloud management, and systems administration skills.