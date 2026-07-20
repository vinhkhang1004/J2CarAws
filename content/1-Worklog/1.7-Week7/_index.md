---
title: "Week 7 Worklog"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---
### Week 7 Objectives:
* Integrate VNPay, Momo, and Stripe payment processors.
* Build order checkouts and transaction links with secure checksum codes.
* Deploy AWS Lambda to capture Webhook (IPN) callbacks in isolation.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Integrate payment libraries and write endpoint URL generator functions for VNPay, MoMo, and Stripe. | 15/06/2026 | 16/06/2026 | Payment Gateway Docs |
| Tuesday | Implement validation logic verifying Checksums and payment keys received in callbacks. | 16/06/2026 | 17/06/2026 | Security Hash Guides |
| Wednesday | Write serverless handler functions in Node.js for AWS Lambda. | 17/06/2026 | 18/06/2026 | AWS Lambda Nodejs |
| Thursday | Deploy AWS Lambda into Private Subnet 5 (Integration Tier) to protect inside resources. | 18/06/2026 | 19/06/2026 | AWS Network Integration |
| Friday | Perform simulated callback testing verifying payload integrity and response statuses. | 19/06/2026 | 19/06/2026 | Payment API Testing |

### Week 7 Achievements:
* Dynamic payment URL creation complete for Momo, VNPay, and Stripe.
* Serverless AWS Lambda webhook handler deployed to Private Subnet 5 (Integration Tier).
* Asynchronous payment ingestion architecture prevents main backend resources from being bogged down by webhooks.
