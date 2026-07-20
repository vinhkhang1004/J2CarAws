---
title: "Week 10 Worklog"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---
### Week 10 Objectives:
* Compile React SPA code and upload static files to S3 Web Bucket.
* Set up Amazon CloudFront CDN distribution to optimize global static content delivery.
* Configure strict CORS parameters on the Express Backend.
* Set up ACM SSL/TLS certificates and configure AWS WAF rules to protect endpoints.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Build React SPA to static assets and upload to S3 Web Bucket with Static Hosting mode active. | 06/07/2026 | 06/07/2026 | React Build & S3 Hosting |
| Tuesday | Update CORS variables on the Express backend server to accept requests only from the official domain. | 07/07/2026 | 07/07/2026 | Express CORS Docs |
| Wednesday | Generate ACM SSL certificate and create Amazon CloudFront CDN Distribution referencing S3 Bucket. | 08/07/2026 | 09/07/2026 | AWS ACM & CloudFront |
| Thursday | Provision AWS WAF Web ACL rules in front of CloudFront CDN and ALB. | 09/07/2026 | 10/07/2026 | AWS WAF Ruleset |
| Friday | Configure security rules against SQL Injection, XSS exploits, and DDoS vectors. | 10/07/2026 | 10/07/2026 | OWASP Top 10 WAF |

### Week 10 Achievements:
* React SPA client assets hosted on S3 and distributed via CloudFront CDN distribution with minimal load time.
* HTTPS transport encryption applied across all user-facing domain routes.
* AWS WAF acts as an edge shield, intercepting malicious requests, automated scans, XSS, and SQLi attempts.
