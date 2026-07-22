---
title: "Blog 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# AWS COST OPTIMIZATION – Why Should Organizations Migrate Amazon EBS Volumes from gp2 to gp3?

Hello everyone!

Amazon Elastic Block Store (Amazon EBS) is one of the most widely used block storage services for Amazon EC2 workloads in production environments. For many years, numerous organizations have continued to run their workloads on **gp2 (General Purpose SSD)** volumes because it was previously the default storage option provided by AWS.

Since the introduction of **gp3**, AWS has consistently recommended customers migrate to this newer generation of General Purpose SSD volumes. Besides offering lower storage costs, gp3 provides more consistent performance and greater flexibility in configuring storage performance. According to the **AWS Cost Optimization Hub**, simply migrating existing EBS volumes from gp2 to gp3 can reduce storage costs by up to **20%**, while improving performance without requiring application changes or service downtime.

---

## 1. Comparing gp2 and gp3 Architecture and Performance

The primary difference between gp2 and gp3 lies in how storage performance is allocated.

### gp2 – Performance Depends on Volume Size

With gp2, storage performance is directly tied to the size of the volume.

Each gp2 volume provides approximately **3 IOPS per GB** of allocated storage.

As a result, applications requiring higher IOPS often need to provision larger volumes, even if additional storage capacity is unnecessary. For example, achieving approximately **3,000 IOPS** requires a volume of around **1,000 GB**, which increases storage costs without delivering additional business value.

### gp3 – Independent Performance Configuration

Unlike gp2, gp3 separates storage capacity from performance.

Each gp3 volume includes by default:

- **3,000 IOPS**
- **125 MB/s Throughput**

regardless of the allocated storage size.

If additional performance is required, users can independently increase IOPS or throughput without expanding storage capacity.

### Quick Comparison

- gp3 storage pricing is approximately **20% lower** than gp2.
- gp2 provides **3 IOPS per GB**, while gp3 delivers **3,000 baseline IOPS** by default.
- gp3 supports configurable throughput up to **1,000 MB/s**.
- Storage capacity, IOPS, and throughput can be configured independently on gp3.

---

## 2. Key Benefits and Recommended Workloads

### Immediate Cost Optimization

Because gp3 storage is priced lower than gp2, organizations can immediately reduce monthly infrastructure expenses, especially when operating hundreds or thousands of EBS volumes.

### Zero-Downtime Migration

Using the **Amazon EBS Elastic Volumes** feature, existing gp2 volumes can be converted directly to gp3 while the EC2 instance remains online.

The migration process does not require:

- Stopping EC2 instances.
- Rebooting servers.
- Restoring data.
- Interrupting application availability.

### Recommended Workloads

Migrating to gp3 is particularly beneficial for:

- Web applications.
- REST API servers.
- MySQL databases.
- PostgreSQL databases.
- SQL Server.
- MongoDB.
- Bastion Hosts.
- Monitoring servers.
- Jenkins workers.
- GitLab Runners.
- File servers.
- Storage nodes.

---

## 3. Recommended Migration Process for DevOps Teams

### Step 1 – Identify Existing gp2 Volumes

Organizations can use the following AWS services to identify gp2 volumes and estimate potential savings:

- AWS Cost Optimization Hub.
- AWS Cost Explorer.
- AWS CLI.

These tools help determine which volumes should be migrated first based on utilization and potential cost reduction.

### Step 2 – Automate the Migration

For environments containing many EBS volumes, automation is strongly recommended instead of performing manual updates through the AWS Management Console.

Common automation options include:

- AWS Systems Manager Automation.
- AWS Lambda.
- AWS CLI.
- Terraform.
- AWS CloudFormation.
- AWS CDK.

When Infrastructure as Code is used, remember to update the volume configuration to:

`volume_type = "gp3"`

This prevents future deployments from recreating gp2 volumes.

### Step 3 – Monitor Performance After Migration

Following migration, system performance should be monitored for approximately **7–14 days** using Amazon CloudWatch.

Important metrics include:

- **VolumeReadOps**
- **VolumeWriteOps**
- **VolumeThroughputPercentage**
- **VolumeConsumedReadWriteOps**

Monitoring these metrics helps determine whether the default 3,000 IOPS is sufficient or if additional IOPS and throughput should be provisioned.

---

## Conclusion

Migrating Amazon EBS volumes from **gp2 to gp3** is one of the simplest and most effective cost optimization opportunities available on AWS.

Organizations can immediately reduce storage costs by approximately **20%**, while gaining more flexible storage performance without changing application architecture or causing service interruption.

If your AWS environment still contains gp2 volumes, now is an excellent time to plan and automate the migration to gp3 in order to improve both infrastructure performance and long-term operational efficiency.

---


## Reference

https://aws.amazon.com/blogs/storage/migrate-your-amazon-ebs-volumes-from-gp2-to-gp3-and-save-up-to-20-on-costs/