---
title: "Week 6 Worklog"
date: 2026-07-06
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Collaborate with the team to deploy the backend onto AWS Lambda, run it serverless, and expose APIs via API Gateway.
* Prepare access permissions and test calling AI services from Lambda.

### Tasks to be carried out this week (07/06/2026 - 07/10/2026):

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | ---------- | --------------- | ----------------------------------------- |
| 2 | - Migrate the backend to run as serverless functions, expose APIs via API Gateway for frontend calls | 07/06/2026 | 07/06/2026 | [Serverless lab](https://000078.awsstudygroup.com), [API Gateway lab](https://000079.awsstudygroup.com) |
| 3 | - Design the minimum required IAM permissions for Lambda to invoke AI services (image recognition, text extraction, Q&A) | 07/07/2026 | 07/07/2026 | [IAM Role](https://000048.awsstudygroup.com) |
| 4 | - Build a test Lambda function to invoke the image content recognition service on sample files, and measure response times | 07/08/2026 | 07/08/2026 | |
| 5 | - Build a test function to invoke the text extraction service on documents/images containing text, and handle various response formats | 07/09/2026 | 07/09/2026 | |
| 6 | - Implement a handling mechanism for cases where AI services fail to respond | 07/10/2026 | 07/10/2026 | |

### Week 6 Achievements:

* The backend runs completely serverless with a public API layer for the frontend, successfully transitioning to cloud-based API calls.
* Established the minimum necessary access permission structure for Lambda to invoke AI services.
* Successfully tested calling image recognition and text extraction services from Lambda, measuring response times and practical limitations.

