---
title: "Week 9 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 9 Objectives:

* Configure Amazon S3 with a least-privilege IAM role for product image storage.
* Deploy the Spring Boot application on EC2 as a managed `systemd` service.

### Tasks to be carried out this week:
| Day | Task                                                                                              | Start Date | Completion Date | Reference Material                        |
| --- | -------------------------------------------------------------------------------------------------- | ---------- | --------------- | ----------------------------------------- |
| 2   | - Created an S3 bucket for product images <br> - Configured a private bucket policy                | 10/06/2025 | 10/06/2025      |
| 3   | - Created a least-privilege IAM Role (`PutObject`/`GetObject` only) <br> - Attached it to the EC2 instance profile | 10/07/2025 | 10/07/2025      | <https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html> |
| 4   | - Implemented image upload & presigned URL generation in the backend (AWS SDK for Java)             | 10/08/2025 | 10/08/2025      | <https://docs.aws.amazon.com/sdk-for-java/> |
| 5   | - Built the deployment jar and deployed it to EC2 <br> - Validated a real image upload end-to-end   | 10/09/2025 | 10/09/2025      |
| 6   | - Wrote the `systemd` unit file <br> - Enabled the app as a managed service with auto-restart        | 10/10/2025 | 10/10/2025      |


### Week 9 Achievements:

* Product images stored in S3 exclusively through a least-privilege IAM role, validated with a real upload test.
* Backend generates presigned URLs so the frontend never talks to S3 directly.
* Application now runs as a resilient `systemd` service on EC2, restarting automatically on failure.
* ...
