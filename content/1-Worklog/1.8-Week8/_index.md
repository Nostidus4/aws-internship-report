---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 8 Objectives:

* Provision the VPC, subnets, and Security Groups for DIY Shop.
* Launch RDS PostgreSQL and EC2, and establish a secure connection between them.

### Tasks to be carried out this week:
| Day | Task                                                                                                | Start Date | Completion Date | Reference Material                        |
| --- | ---------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| 2   | - Created a VPC with 2 public + 2 private subnets across 2 AZs <br> - Configured route tables & IGW    | 09/29/2025 | 09/29/2025      | <https://docs.aws.amazon.com/vpc/> |
| 3   | - Created Security Groups: EC2 (public, inbound HTTP/SSH) and RDS (private, inbound only from EC2 SG) | 09/30/2025 | 09/30/2025      |
| 4   | - Provisioned RDS PostgreSQL (`db.t4g.micro`) inside the private subnet                                | 10/01/2025 | 10/01/2025      | <https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_GettingStarted.html> |
| 5   | - Launched an EC2 instance (`t3.micro`) in the public subnet <br> - Attached an Elastic IP              | 10/02/2025 | 10/02/2025      |
| 6   | - Verified secure EC2→RDS connectivity over the private network <br> - Ran `flyway migrate` against the real RDS instance | 10/03/2025 | 10/03/2025      |


### Week 8 Achievements:

* VPC/subnet/Security Group topology provisioned across 2 Availability Zones.
* RDS PostgreSQL reachable only from the application tier, never from the public internet.
* Application schema successfully migrated onto the real RDS instance via Flyway.
* ...
