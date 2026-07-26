---
title: "Week 7 Worklog"
date: 2026-07-13
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Collaborate with the team to integrate DynamoDB for file metadata storage.
* Officially integrate the AI layer (image recognition, text extraction) into the upload workflow and store results associated with metadata.

### Tasks to be carried out this week (07/13/2026 - 07/17/2026):

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | ---------- | --------------- | ----------------------------------------- |
| 2 | - Create a DynamoDB database to store file information, and connect the backend to write/retrieve metadata | 07/13/2026 | 07/13/2026 | [DynamoDB lab](https://000078.awsstudygroup.com) |
| 3 | - Design the schema to store AI analysis results (image labels, extracted text) in DynamoDB, ensuring separation and consistency with the original file metadata | 07/14/2026 | 07/14/2026 | |
| 4 | - Officially integrate the image content recognition service into the upload workflow to automatically tag and store results along with file metadata | 07/15/2026 | 07/15/2026 | [AI services](https://000056.awsstudygroup.com) |
| 5 | - Officially integrate the text extraction service for documents and images containing text, and store the extracted text with metadata | 07/16/2026 | 07/16/2026 | |
| 6 | - Test the entire image recognition and text extraction workflow with various file types, and handle unsupported file cases | 07/17/2026 | 07/17/2026 | |

### Week 7 Achievements:

* File information is stored and queried from DynamoDB, separated from the file content on the storage platform.
* Designed a separate schema for storing AI results that remains consistent with the original metadata.
* Uploaded images are automatically tagged and documents automatically extracted for text; tested successfully across various file types and unsupported scenarios.

