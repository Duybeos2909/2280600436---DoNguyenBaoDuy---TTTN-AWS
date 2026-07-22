---
title: "Blog 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# AWS BACKUP – AWS Backup Adds Item-Level Recovery for Amazon EBS and Amazon S3

Hello everyone!

One of the most common situations when operating cloud systems is the accidental deletion of data by users or applications. It may only be a configuration file, a log file, a PDF document, or a video stored on Amazon EBS or Amazon S3. However, restoring a single file has traditionally been far from straightforward.

For Amazon EBS Snapshots or backups managed by AWS Backup, administrators previously had to restore the entire volume, attach it to an EC2 instance, and then manually locate and copy the required file. This process consumed additional storage resources, increased recovery time, and generated unnecessary operational costs.

To address this challenge, AWS introduced **AWS Backup Search** and **Item-Level Recovery (ILR)**, enabling administrators to search and restore individual files directly from Amazon EBS and Amazon S3 backups.

---

## 1. WHAT IS ITEM-LEVEL RECOVERY AND WHEN IS IT USEFUL?

Item-Level Recovery (ILR) is the ability to restore individual files or objects instead of recovering an entire backup.

With this capability, administrators no longer need to restore an entire Amazon EBS volume containing hundreds of gigabytes or even terabytes of data simply to retrieve a single file.

This feature is particularly valuable in several real-world scenarios.

### Recovering Accidentally Deleted Files

If an employee accidentally deletes an application configuration file or an important business document stored on an EC2 volume, administrators can simply search for that specific file within AWS Backup and restore it within minutes.

### Supporting Audit and Incident Investigation

Organizations often need to retrieve historical documents such as PDF contracts, Excel reports, surveillance videos, or exported CSV files.

Instead of restoring a complete snapshot, administrators can directly locate the required file using AWS Backup Search.

### Reducing Recovery Time Objective (RTO)

Item-Level Recovery significantly shortens recovery time by restoring only the required files.

This reduces production downtime from hours to only a few minutes when accidental file deletion occurs.

---

## 2. HOW IT WORKS AND IMPLEMENTATION BEST PRACTICES

To locate files without scanning an entire snapshot, AWS Backup relies on **metadata indexing** during the backup process.

Before using Item-Level Recovery, several important considerations should be taken into account.

### Enable Backup Indexing

Backup Indexing is a prerequisite for Item-Level Recovery.

When creating a Backup Plan or running an On-Demand Backup, administrators should enable indexing so AWS Backup can catalog metadata for every file contained in the backup.

### Apply Consistent Resource Tagging

Resources such as EC2 Instances, Amazon EBS Volumes, and Backup Vaults should use consistent tagging strategies.

Proper tagging simplifies resource management and makes searching much easier in environments containing multiple applications and workloads.

### Search Files with AWS Backup Search

AWS Backup Search allows administrators to locate files using various search criteria, including:

- File name
- Directory path
- File type
- Backup time
- Metadata

Once the desired file has been located, Item-Level Recovery can restore only that file without restoring the complete backup.

### Improve Operational Resilience

To maximize data protection, AWS recommends combining Item-Level Recovery with additional best practices, including:

- Creating appropriate Backup Plans.
- Performing regular restore testing.
- Using AWS Backup Vault Lock to protect backups against ransomware and accidental deletion.

---

## CONCLUSION

AWS Backup Search and Item-Level Recovery represent a significant enhancement for DevOps and Cloud Operations teams.

Instead of restoring an entire snapshot simply to recover a single file, administrators can now quickly search for and restore exactly the data they need.

This capability helps reduce operational costs, minimize recovery time, improve Recovery Time Objectives (RTO), and simplify backup management across cloud environments.

---

## Architecture Overview

![AWS Backup Item-Level Recovery](/images/3-Blog/AWS-Backup-ILR.png)

---

## Reference

https://aws.amazon.com/blogs/storage/enable-item-level-search-and-recovery-for-amazon-ec2-with-aws-backup/