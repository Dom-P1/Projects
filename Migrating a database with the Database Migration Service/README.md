# 🔄 AWS Database Migration Using DMS

This project documents the migration of a relational database using **AWS Database Migration Service (DMS)**. It demonstrates how to replicate data from an on-premises or self-hosted database to an AWS RDS instance.

---

## 📘 Overview

**Problem:** Migrate an existing database with minimal downtime to AWS.

**Solution:** Use AWS DMS to perform a full load and ongoing replication from the source database to an Amazon RDS target.

---

## 🏗️ Architecture

![Architecture Diagram](architecture.png)

### Flow Summary:
- Source database: On-premises or EC2-hosted MySQL/PostgreSQL
- AWS DMS Replication Instance performs data migration
- Target database: Amazon RDS (MySQL/PostgreSQL)
- CloudWatch used for replication monitoring

---

## 🛠️ AWS Services Used

- **AWS DMS** – Data migration and replication
- **Amazon RDS** – Target database
- **Amazon EC2** – (Optional) Source DB host
- **CloudWatch** – Monitor replication task progress and errors
- **IAM** – Permissions for DMS to access source and target

---

## 🔐 Security Practices

- **Source/Target DB** accessed via secure endpoints (SSL)
- **Replication Instance** placed in private subnet within VPC
- **IAM Role** created with required policies for DMS
- **CloudWatch Alarms** configured to track replication lag/errors

---

## 🎥 Walkthrough Video

Instead of static screenshots, this project includes a **recorded walkthrough video** showing the full process of using AWS DMS to migrate a database.

The video covers:
- Setting up source and target endpoints
- Creating the DMS replication instance
- Configuring and launching the migration task
- Monitoring progress via CloudWatch and the DMS console

📹 https://youtu.be/SkcZJ2UwZ6Q

---

## 🧠 Lessons Learned

- Learned how to migrate production databases with low downtime
- Understood DMS task phases: Full Load, CDC (Change Data Capture)
- Practiced IAM scoping for DMS access to endpoints
- Identified common migration issues (schema mismatches, data type differences)

---

## ✍️ Author

Dominic Pinedo
