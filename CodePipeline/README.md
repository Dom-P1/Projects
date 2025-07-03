# 🚀 AWS CodePipeline CatPipeline

A fully automated CI/CD pipeline project built using AWS Developer Tools like CodePipeline, CodeBuild, and CloudFormation. Inspired by Adrian Cantrill’s advanced AWS demo.

---

## 📘 Overview

**Problem:** Developers need a secure and automated way to build, test, and deploy serverless applications on AWS.  
**Solution:** A robust CI/CD pipeline using AWS CodePipeline, triggered by GitHub commits, which builds and deploys infrastructure using CloudFormation.

---

## 🏗️ Architecture

![Architecture Diagram](architecture.png)

### Flow Summary:
- Code commit on GitHub triggers CodePipeline
- CodePipeline runs CodeBuild for lint/test/validate
- CodeBuild packages and uploads to S3
- CloudFormation deploys infrastructure (Lambda, API Gateway, etc.)
- IAM roles scoped tightly for each stage

---

## 🛠️ AWS Services Used

- **AWS CodePipeline** – CI/CD orchestration
- **AWS CodeBuild** – Build and validation steps
- **AWS CloudFormation** – Infrastructure as Code deployment
- **Amazon S3** – Stores packaged artifacts
- **IAM** – Scoped role access for build and deploy
- **CloudWatch** – Build logs and pipeline notifications

---

## 🔐 Security Practices

- IAM roles are scoped per stage of the pipeline
- Build artifacts are stored in private S3 buckets
- CloudFormation uses service roles for deployment
- Logging and build reports via CloudWatch

---

## 📸 Screenshots

Screenshots of AWS Console setup are available in the `/screenshots` folder.

---

## 📚 Lessons Learned

- Automated multi-stage CI/CD pipeline on AWS
- Integrated GitHub as a pipeline source
- Used CodeBuild for packaging and testing
- Managed infrastructure using CloudFormation templates

---

## ✍️ Author

Your Name – DevOps & Cloud Engineer  
[LinkedIn](https://linkedin.com) | [Portfolio](https://yourportfolio.com)
