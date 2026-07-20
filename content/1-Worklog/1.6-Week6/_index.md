---
title: "Week 6 Worklog"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---
### Week 6 Objectives:
* Create image upload API for capturing damaged auto parts.
* Develop keyword, metadata, and file name parsing algorithm to recognize the auto part type.
* Run DocumentDB queries to fetch compatible replacement suggestions.
* Configure temporary image storage in Amazon S3 for review and quality control.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | Build the `/api/upload/scan-image` API endpoint to collect uploaded images from clients. | 09/06/2026 | 09/06/2026 | Express Upload API |
| Tuesday | Develop metadata, EXIF data, and filename parsing scripts to classify auto parts keywords. | 10/06/2026 | 11/06/2026 | Image Parsing Logic |
| Wednesday | Construct database lookup requests to fetch alternative replacements matching the keywords. | 11/06/2026 | 12/06/2026 | DocumentDB Query Builders |
| Thursday | Save scanning upload assets in Amazon S3 Media Bucket for diagnostics and testing. | 12/06/2026 | 13/06/2026 | AWS S3 Integration |
| Friday | Perform end-to-end integration testing on image classification recommendations. | 13/06/2026 | 13/06/2026 | Feature Testing |

### Week 6 Achievements:
* Finished the AI Scan Image endpoint pipeline.
* Keyword mapping matches typical replacement categories (brakes, filters, spark plugs, tires, headlights).
* The user is automatically prompted with replacement components.
* Asset storage configured securely on Amazon S3.
