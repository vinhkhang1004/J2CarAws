---
title: "Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

### Project Overview

The J2Car AutoParts system is designed using a Microservices/Containerized architecture running on Amazon Web Services (AWS), ensuring High Availability, robust security, and Auto Scaling.

**Key Request Handling Flow:**
* **Frontend Access:** The React Single Page Application (SPA) is compiled and hosted on an Amazon S3 Web Bucket, distributed globally via Amazon CloudFront, and protected by AWS WAF.
* **Business Logic (Backend):** REST APIs and Socket.io connections are routed through an Application Load Balancer (ALB) (supporting Sticky Sessions) to ECS Backend Task containers (NodeJS + Express) running on AWS Fargate within secure Private Subnets.
* **Asynchronous Payments (Payment Integration):** External payment gateways (Momo, VNPay, Stripe) send IPN Webhooks to AWS Lambda. Lambda receives, validates, and pushes clean invoice logs to Amazon SQS (Payment Queue). ECS Fargate Backend Tasks act as Workers to pull messages from the SQS queue, finalize orders, and update real-time status via Socket.io.
* **Data Storage:** Document data is stored in Amazon DocumentDB (MongoDB-compatible) in a cluster with a Primary Node (read/write) and Replica Nodes (read-only) synced automatically. Session caching and Socket.io connection state management are handled by Amazon ElastiCache Redis (Primary/Replica).

---

### Worklog (12 Weeks)

Below is the detailed progress by week:

**Week 1 (05/05/2026 - 11/05/2026):** [System Initialization & AWS Explore Basics](1.1-week1/)

**Week 2 (12/05/2026 - 18/05/2026):** [Practical VPC, EC2 & Basic Databases](1.2-week2/)

**Week 3 (19/05/2026 - 25/05/2026):** [DynamoDB, CDN CloudFront & AWS Office Day (24/05)](1.3-week3/)

**Week 4 (26/05/2026 - 01/06/2026):** [Auto Scaling, DNS Route 53 & Security WAF/Secrets Manager](1.4-week4/)

**Week 5 (02/06/2026 - 08/06/2026):** [Serverless Lambda, SQS & AWS Office Day (07/06)](1.5-week5/)

**Week 6 (09/06/2026 - 15/06/2026):** [AI Image Scanning & Auto Parts Identification Algorithm Integration](1.6-week6/)

**Week 7 (16/06/2026 - 22/06/2026):** [External Payment Gateways & Webhook (IPN) Integration](1.7-week7/)

**Week 8 (23/06/2026 - 29/06/2026):** [Transaction Processing Queue & Asynchronous Worker Construction](1.8-week8/)

**Week 9 (30/06/2026 - 06/07/2026):** [Docker Containerization & ECS Fargate Deployment](1.9-week9/)

**Week 10 (07/07/2026 - 13/07/2026):** [Frontend Deployment, CDN Configuration & Web Application Firewall Setup](1.10-week10/)

**Week 11 (14/07/2026 - 20/07/2026):** [Disaster Recovery Testing & High Availability Verification](1.11-week11/)

**Week 12 (21/07/2026 - 30/07/2026):** [Performance Optimization, Database Scaling & System Monitoring](1.12-week12/)
