---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---
### Week 8 Objectives:
* Deploy Amazon SQS as a messaging queue storing invoice receipts.
* Construct a Worker service connecting to SQS to process payments asynchronously.
* Email order receipts using Nodemailer and push live dashboard update events via Socket.io.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Provision Amazon SQS (Payment Queue) queue broker with appropriate retention policy. | 23/06/2026 | 23/06/2026 | AWS SQS Console |
| Tuesday | Update Lambda callback code to parse and publish payment messages directly to SQS. | 24/06/2026 | 24/06/2026 | AWS SDK SQS publisher |
| Wednesday | Implement asynchronous polling worker service listening to SQS queue messages. | 25/06/2026 | 26/06/2026 | SQS Consumer Module |
| Thursday | Write logic updating order database status and clearing relevant user cart caches in Redis. | 26/06/2026 | 27/06/2026 | Order Management Docs |
| Friday | Add Nodemailer email delivery triggers and broadcast Socket.io update messages to admin workspace. | 27/06/2026 | 27/06/2026 | Nodemailer & Socket.io |

### Week 8 Achievements:
* Amazon SQS configured, successfully decoupling payment gateway triggers from primary servers.
* Message consumer worker runs reliably, preventing double processing of checkouts.
* Instant email alerts are delivered to clients, and administrators get immediate dashboard updates.
