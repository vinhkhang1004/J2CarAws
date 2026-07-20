---
title: "Week 12 Worklog"
date: 2024-01-01
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---
### Week 12 Objectives:
* Refactor database queries and launch DocumentDB Replica instances for read routing.
* Load test SQS payment workflows and ECS tasks scaling thresholds.
* Build AWS CloudWatch dashboards and customize email alerts for anomalies.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Wednesday | Optimize read queries at the codebase level and implement compound index strategies. | 21/07/2026 | 23/07/2026 | DB Query Tuning |
| Thursday | Execute peak load tests sending thousands of checkout requests through SQS queue limits. | 24/07/2026 | 27/07/2026 | Load Testing Tools |
| Friday | Provision secondary DocumentDB Replica Nodes and ElastiCache Redis replication partners across Availability Zones. | 28/07/2026 | 30/07/2026 | AWS Replication Setup |
| Friday | Configure AWS CloudWatch status boards monitoring system resource utilization and deploy automated email alarms. | 28/07/2026 | 30/07/2026 | AWS CloudWatch Alerts |

### Week 12 Achievements:
* Read/write splitting implemented via DB replicas, reducing read response times by 40%.
* Database compound indexes reduce query latency on complex search requests from hundreds of ms to under 10ms.
* Peak load testing successfully processed thousands of requests without bottlenecks or message drop.
* Proactive infrastructure monitoring implemented using CloudWatch charts with email triggers.
