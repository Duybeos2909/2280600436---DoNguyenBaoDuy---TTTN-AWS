---
title: "Blogs Posted"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

This section presents the AWS blogs that I researched, summarized, and shared during my internship. The topics mainly focus on AWS Storage, Security, Backup, and Cost Optimization, helping developers and cloud engineers understand the latest AWS updates and best practices.

### [Blog 1 - Amazon S3 Disables SSE-C by Default for New Buckets](3.1-Blog1/)

This blog introduces an important security update from AWS regarding Amazon S3. Beginning in April 2026, newly created S3 General Purpose Buckets will have **Server-Side Encryption with Customer-Provided Keys (SSE-C)** disabled by default. The article explains the reasons behind this change, its impact on existing applications, and the recommended migration path toward **SSE-S3** and **SSE-KMS** to improve security, simplify key management, and reduce configuration risks.

### [Blog 2 - AWS Backup Item-Level Recovery for Amazon EBS and Amazon S3](3.2-Blog2/)

This blog introduces the new **AWS Backup Search** and **Item-Level Recovery** capabilities for Amazon EBS and Amazon S3. Instead of restoring an entire backup volume, administrators can now search for and recover individual files directly from AWS Backup. The article discusses practical use cases, backup indexing, search capabilities, recovery workflows, and best practices for improving Recovery Time Objective (RTO) while reducing operational costs.

### [Blog 3 - Amazon EBS Cost Optimization: Migrating from gp2 to gp3](3.3-Blog3/)

This blog explains why organizations should migrate Amazon EBS volumes from **gp2** to **gp3**. It compares the performance model, storage pricing, IOPS configuration, and throughput flexibility between the two volume types. The article also provides migration recommendations, automation approaches using Infrastructure as Code (IaC), and monitoring strategies with Amazon CloudWatch to help reduce storage costs by up to 20% while maintaining zero downtime.

---

# Translated Blogs

During the internship, I also translated and studied several technical articles published on the official AWS Blog. These articles helped me gain a deeper understanding of new AWS features and modern cloud architecture.

### Blog 1 - Session Policies in Amazon EKS Pod Identity

This article explains the newly introduced **Session Policies** feature in Amazon EKS Pod Identity. It demonstrates how Kubernetes workloads can share IAM roles while applying fine-grained permission restrictions for individual pods. By combining IAM roles with session policies, organizations can better implement the Principle of Least Privilege, simplify IAM role management, and reduce permission complexity in large Amazon EKS clusters.

### Blog 2 - AWS Backup Search and Item-Level Recovery for Amazon EBS and Amazon S3

This translated article presents the architecture and workflow behind the new **AWS Backup Search** capability. It explains how AWS indexes backup metadata to enable direct file searching and recovery from Amazon EBS and Amazon S3 backups. The article also introduces deployment considerations, backup indexing, recovery workflows, and operational best practices for enterprise backup strategies.

### Blog 3 - Migrate Your Amazon EBS Volumes from gp2 to gp3 and Save up to 20% on Costs

This translated article focuses on AWS recommendations for migrating Amazon EBS volumes from **gp2** to **gp3**. It analyzes the architectural improvements of gp3, explains how performance is decoupled from storage capacity, and demonstrates how organizations can reduce infrastructure costs while improving storage performance. The article also introduces migration planning, automation techniques, and monitoring practices using AWS services.