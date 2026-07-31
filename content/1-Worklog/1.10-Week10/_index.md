---
title: "Week 10 Worklog"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 10 Objectives:

* Set up CloudWatch Agent, log groups, metric filters, and alarms with SNS email alerts.
* Build a GitHub Actions CI/CD pipeline for automated build, test, and deploy.

### Tasks to be carried out this week:
| Day | Task                                                                                                | Start Date | Completion Date | Reference Material                        |
| --- | ---------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| 2   | - Installed & configured CloudWatch Agent on EC2 <br> - Shipped application/access logs to a Log Group | 10/13/2025 | 10/13/2025      | <https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/Install-CloudWatch-Agent.html> |
| 3   | - Created Metric Filters to derive an error-count metric from application logs                        | 10/14/2025 | 10/14/2025      |
| 4   | - Created a CloudWatch Alarm on the error metric <br> - Created an SNS topic + email subscription      | 10/15/2025 | 10/15/2025      | <https://docs.aws.amazon.com/sns/latest/dg/welcome.html> |
| 5   | - Wrote the GitHub Actions workflow: build & test using a PostgreSQL service container                 | 10/16/2025 | 10/16/2025      | <https://docs.github.com/actions> |
| 6   | - Extended the workflow to deploy automatically to EC2 on every push to `main`                         | 10/17/2025 | 10/17/2025      |


### Week 10 Achievements:

* CloudWatch centralizes application and access logs, with metric filters deriving a real-time error-count metric.
* Verified the alarm fires a real email notification via SNS when the error rate crosses the threshold.
* Every push to `main` is automatically built, tested against a PostgreSQL container, and deployed to EC2.
* ...
