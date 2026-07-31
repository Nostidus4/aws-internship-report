---
title: "Week 11 Worklog"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 11 Objectives:

* Move credentials into Secrets Manager and enable Multi-AZ on RDS.
* Add an Application Load Balancer + Auto Scaling Group, and attach AWS WAF.

### Tasks to be carried out this week:
| Day | Task                                                                                                | Start Date | Completion Date | Reference Material                        |
| --- | ---------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| 2   | - Migrated DB & seller credentials from plaintext files to Secrets Manager <br> - Enabled automatic rotation | 10/20/2025 | 10/20/2025      | <https://docs.aws.amazon.com/secretsmanager/> |
| 3   | - Enabled RDS Multi-AZ on the existing instance <br> - Verified failover behavior                     | 10/21/2025 | 10/21/2025      |
| 4   | - Created an Application Load Balancer + Target Group <br> - Created an Auto Scaling Group across 2 AZs | 10/22/2025 | 10/22/2025      | <https://docs.aws.amazon.com/elasticloadbalancing/> |
| 5   | - Created a WAF Web ACL with managed rule groups, attached it to the ALB <br> - Added a rate-limit rule on the login endpoint | 10/23/2025 | 10/23/2025      | <https://docs.aws.amazon.com/waf/> |
| 6   | - Load-tested the Auto Scaling Group's scale-out behavior <br> - Verified TLS termination at the ALB  | 10/24/2025 | 10/24/2025      |


### Week 11 Achievements:

* No plaintext credentials remain on EC2; DB and seller credentials rotate automatically via Secrets Manager.
* Eliminated the RDS single point of failure by enabling Multi-AZ.
* Application tier now runs behind an ALB with TLS termination and an Auto Scaling Group across 2 AZs.
* AWS WAF actively filters application-layer attacks and rate-limits the login endpoint.
* ...
