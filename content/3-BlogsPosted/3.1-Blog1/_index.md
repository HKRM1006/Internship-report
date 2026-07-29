---
title: "AMAZON GUARDDUTY – INTELLIGENT THREAT DETECTION SERVICE"
date: 2026-07-22
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---
# AMAZON GUARDDUTY – INTELLIGENT THREAT DETECTION SERVICE

Amazon GuardDuty is a fully managed threat detection service provided by AWS. It continuously monitors your accounts, workloads, and data for malicious or unauthorized behavior. The key advantage of Amazon GuardDuty is that it requires no agent installation, no additional infrastructure deployment, and no log analysis server maintenance - simply activate the service.

Key takeaways:

* **Automatic Collection:** Automatically gathers data from VPC Flow Logs, CloudTrail event logs, DNS logs, and more.
* **Intelligent Analysis:** Processes data using AWS Machine Learning models and Threat Intelligence.
* **Detection & Alerting:** Compares behavior against known attack patterns and generates alerts complete with severity levels.
* **Comprehensive Risk Detection:** Flags compromised EC2 instances, suspected IAM credential leaks, sudden spikes in S3 requests from unfamiliar IPs, or anomalous behavior on EKS/Containers.
* **Automated Response:** Integrates seamlessly with Amazon EventBridge to automatically isolate infected instances or trigger instant notifications through configured channels.

**Real-world example:**

Suppose one of your EC2 instances suddenly and silently sends traffic to a blacklisted IP address. Instead of manually sifting through millions of log lines, GuardDuty automatically detects this and triggers an alert:

`UnauthorizedAccess:EC2/MaliciousIPCaller.Custom`

...complete with its severity level and actionable remediation steps for your operations team!

### References

* [AWS GuardDuty Docs](https://docs.aws.amazon.com/guardduty/)
* [AWS GuardDuty Overview](https://aws.amazon.com/guardduty/)

### Blog link

[AWS Study Group VN | AMAZON GUARDDUTY – DỊCH VỤ PHÁT HIỆN MỐI ĐE DỌA THÔNG MINH | Facebook](https://www.facebook.com/groups/awsstudygroupfcj/posts/2219986985432928)

### Picture

![Blog1](/images/blog1.png)
