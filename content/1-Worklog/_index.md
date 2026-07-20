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

**Week 1 (05/05/2026 - 10/05/2026):** [Familiarize with the internship environment, work culture at FCAJ, and project workflows. Learn general AWS concepts, basic cloud services, and complete initial exercises to get comfortable with the technologies and workspace.](1.1-week1/)

**Week 2 (11/05/2026 - 17/05/2026):** [Continue implementing small tasks and studying foundational AWS services including IAM, EC2, and S3. Understand resource management, data storage, and user permission configurations through basic hands-on labs.](1.2-week2/)

**Week 3 (18/05/2026 - 24/05/2026):** [Work directly on-site at the office, continue studying AWS services, and perform practical exercises related to VPC, RDS, and CloudWatch to understand networking, databases, and system monitoring.](1.3-week3/)

**Week 4 (25/05/2026 - 31/05/2026):** [Study advanced AWS configurations and complete hands-on labs covering Elastic Load Balancing (ALB), Auto Scaling, Route 53, Lambda, and container orchestration services like Amazon ECS. Understand cloud deployment architecture and system scalability.](1.4-week4/)

**Week 5 (01/06/2026 - 07/06/2026):** [Research business operations and the enterprise ecosystem. Study system design principles, security strategies, software architecture, and product development lifecycles in real-world environments through serverless and secure storage services.](1.5-week5/)

**Week 6 (08/06/2026 - 14/06/2026):** [Begin business analysis and brainstorming for the hands-on project (Workshop). Analyze system requirements for the J2Car AutoParts e-commerce application, design core APIs, and implement the AI Scan Image feature to identify damaged auto parts.](1.6-week6/)

**Week 7 (15/06/2026 - 21/06/2026):** [Continue finalizing the analysis and system architecture of the J2Car AutoParts project. Integrate third-party payment gateways (Momo, VNPay, Stripe), implement secure Checksum hashing algorithms, and deploy AWS Lambda Serverless as a webhook IPN within a secure network tier.](1.7-week7/)

**Week 8 (22/06/2026 - 28/06/2026):** [Complete the system design for J2Car AutoParts, designing a decoupled payment flow using Amazon SQS queues. Develop a Backend Worker module to poll SQS messages, automate order processing, clear cart caches in Redis, trigger Nodemailer emails, and push real-time updates via Socket.io.](1.8-week8/)

**Week 9 (29/06/2026 - 05/07/2026):** [Start developing and containerizing the J2Car AutoParts Backend using Docker. Deploy and run serverless container tasks on Amazon ECS Fargate behind an ALB with Cookie Sticky Sessions to ensure stable WebSocket chat connections.](1.9-week9/)

**Week 10 (06/07/2026 - 12/07/2026):** [Perform end-to-end deployment of J2Car AutoParts on AWS: host React SPA Frontend on S3 Web Hosting, distribute globally via CloudFront CDN over HTTPS, and assign AWS WAFv2 rulesets to block SQL Injection, XSS, and bot scans.](1.10-week10/)

**Week 11 (13/07/2026 - 19/07/2026):** [Execute functional and integration tests across the deployed J2Car AutoParts application. Simulate Availability Zone (AZ) failure scenarios to verify disaster recovery (DR) and automatic failover behaviors of the VPC, ECS Fargate, and DocumentDB databases.](1.11-week11/)

**Week 12 (20/07/2026 - 27/07/2026):** [Finalize the J2Car AutoParts project by performing peak load tests, verifying system functionalities, and optimizing database performance via MongoDB indexes and DocumentDB/Redis replica read routing. Set up CloudWatch charts and alarms for proactive resource monitoring.](1.12-week12/)
