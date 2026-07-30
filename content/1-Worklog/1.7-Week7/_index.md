---
title: "Week 7 Worklog"
date: 2026-07-27
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Integrate VNPay Sandbox payment gateway for the Shopsflow order payment workflow.
* Implement Return URL handling endpoints and Webhook IPN (Instant Payment Notification) to automatically update order statuses and restore stock upon payment failure or cancellation.
* Document VNPay payment integration workflows, write Clean-up procedures, and complete integration testing.

### Tasks to be implemented this week:

| Day | Tasks | Start Date | End Date |
| :---: | :--- | :---: | :---: |
| **Mon** | - Research VNPay Sandbox payment documentation, register Sandbox credentials, and configure environment keys (`VNPAY_TMN_CODE`, `VNPAY_HASH_SECRET`, `VNPAY_API_URL`, `VNPAY_RETURN_URL`) in `.env` | 27/07/2026 | 27/07/2026 |
| **Tue** | - Develop `VnPayUtil` utility generating secure SHA512 signatures and backend endpoint creating payment checkout URLs (`createPaymentUrl`) | 28/07/2026 | 28/07/2026 |
| **Wed** | - Implement response processing endpoints: Return URL and Webhook IPN (updating order status to `PAID` or `CANCELLED`, restoring product inventory on payment cancellation) | 29/07/2026 | 29/07/2026 |
| **Thu** | - Execute test transactions using VNPay Sandbox test bank cards; author VNPay integration guide (`VNPAY_INTEGRATION.md`) | 30/07/2026 | 30/07/2026 |
| **Fri** | - Author Unit Tests for `VnPayService` (`VnPayServiceTest`), execute comprehensive Maven backend integration tests, and draft Clean-up procedures | 31/07/2026 | 31/07/2026 |

### Week 7 Achievements:

* Successfully integrated VNPay Sandbox online payment gateway into Shopsflow order checkout.
* Built automated Webhook verification mechanism validating VNPay SHA512 digital signatures during IPN callbacks.
* Completed detailed integration guide (`VNPAY_INTEGRATION.md`) enabling smooth Frontend (React) payment result screen implementation.
* Entire Backend system passed End-to-End integration testing with complete resource Clean-up procedures.