---
title: "Week 9 Worklog"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---
### Week 9 Objectives:
* Package the NodeJS Express app inside optimized Dockerfiles.
* Configure ECS Task Definitions and launch service on AWS Fargate.
* Configure Application Load Balancer (ALB) with Sticky Sessions.
* Configure ECS Auto Scaling rules and NAT Gateways for secure outbound routes.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Write multi-stage Dockerfile to minimize container size for the Express Backend. | 30/06/2026 | 30/06/2026 | Docker Guide |
| Tuesday | Push release images to Amazon ECR registry and specify ECS Task Definition settings. | 01/07/2026 | 01/07/2026 | AWS ECR & Task Definitions |
| Wednesday | Configure Application Load Balancer (ALB) with Cookie Sticky Sessions for Socket.io traffic stability. | 02/07/2026 | 03/07/2026 | AWS ALB Documentation |
| Thursday | Deploy ECS service running 2 Tasks Backend NodeJS in Private Subnet 1 and Private Subnet 2 across two different AZs. | 03/07/2026 | 04/07/2026 | AWS ECS Fargate Deploy |
| Friday | Apply ECS Auto Scaling policies based on resource consumption and launch dual NAT Gateways. | 04/07/2026 | 04/07/2026 | AWS NAT Gateway & Scaling |

### Week 9 Achievements:
* Production Docker image size optimized under 150MB and stored in ECR.
* Backend hosted securely on serverless AWS Fargate task containers.
* ALB distributes requests correctly; Sticky Sessions maintain stable WebSocket chat connectivity.
* Internal containers establish outbound network routes safely through NAT Gateways.
