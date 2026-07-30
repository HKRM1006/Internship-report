---
title: "CROSS-ACCOUNT SAGEMAKER PIPELINE MONITORING – INTEGRATING CUSTOM CLOUDWATCH DASHBOARDS"
date: 2026-07-30
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# CROSS-ACCOUNT SAGEMAKER PIPELINE MONITORING – INTEGRATING CUSTOM CLOUDWATCH DASHBOARDS

In organizations adopting MLOps, Amazon SageMaker Pipelines is commonly used to automate model training and deployment workflows while distributing these workloads across multiple AWS accounts and Regions to isolate development, test, and production environments. However, this distribution introduces a significant monitoring challenge: operations teams must constantly switch between multiple accounts and Regions to track the progress of each pipeline, which is time-consuming and prone to missing issues.

Key takeaways:

* **Hub-and-spoke architecture:** A primary central account/Region acts as the monitoring hub, while lightweight components are deployed in each secondary account/Region (spoke) to collect pipeline data and forward it back to the hub.
* **Serverless, event-driven:** The solution responds immediately to SageMaker Pipeline events instead of polling or maintaining an always-on monitoring infrastructure, reducing operational costs and maintenance overhead.
* **Dashboard stack (at the hub):** Consists of a CloudWatch dashboard, an Amazon DynamoDB storage table, and AWS Lambda functions for processing/rendering data—deployed exclusively in the central account/Region.
* **Forwarder stack (at the spokes):** Deployed in the monitored accounts, using Amazon EventBridge to send processed data back to the monitoring hub.
* **Cross-account event flow:** When a pipeline step changes state, SageMaker AI generates an event with metadata (timestamp, pipeline ARN, step status, etc.); EventBridge at the source account captures the event, Lambda processes and enriches the information, and then forwards it via EventBridge to the central hub account—all secured by AWS IAM roles and policies.
* **Storage and visualization at the hub:** The hub Lambda ingests data and saves it into DynamoDB (Region, account ID, creation/start/end times, display name, execution status, and step statuses) while also serving as the backend for the dashboard, returning an HTML interface rendered as a custom CloudWatch widget.
* **User experience:** Enables filtering by pipeline name and viewing detailed step information (name, type, duration, status) directly within the AWS Management Console without switching accounts or Regions.
* **Automated alerting:** CloudWatch can trigger alarms and send notifications via Amazon SNS when anomalous user activity is detected on the dashboard.

**Real-world example:**

An organization has 3 separate AWS accounts for Dev, Test, and Production environments, with each account running different SageMaker Pipelines for model training. Instead of the operations team logging into each account individually to check pipeline statuses, the hub-and-spoke architecture aggregates all statuses—from Dev to Production—into a single CloudWatch dashboard at the central account. This allows teams to instantly detect failed or slow-running pipelines without ever leaving the central console.

### References

* [AWS Machine Learning Blog - Monitor Amazon SageMaker Pipelines Cross-Account with Custom Amazon CloudWatch Dashboards](https://aws.amazon.com/blogs/machine-learning/monitor-amazon-sagemaker-pipelines-cross-account-with-custom-amazon-cloudwatch-dashboards/)

### Article Link

[GIÁM SÁT SAGEMAKER PIPELINES ĐA TÀI KHOẢN: TÍCH HỢP CLOUDWATCH DASHBOARD TÙY CHỈNH](https://www.facebook.com/groups/awsstudygroupfcj/posts/2228796084552018/)

### Image

![Blog3](/images/blog3.PNG)

