# 🐱🚀 CatPipeline: CI/CD with AWS CodeCommit, CodeBuild, CodeDeploy, and ECS

This project implements a fully managed CI/CD pipeline for containerized applications using **AWS native DevOps tools**: CodeCommit, CodeBuild, CodeDeploy, and ECS with Fargate.

---

## 📘 Overview

**Goal:** Automate the build, test, and deployment of a containerized web app to Amazon ECS using an AWS-native pipeline.

---

## 🏗️ Architecture

![Architecture Diagram](architecture.png)

### Pipeline Steps:
1. **Developer pushes code to CodeCommit**
2. **CodeBuild** builds the Docker image and pushes it to **Amazon ECR**
3. **CodeDeploy** triggers deployment to **Amazon ECS (Fargate)**
4. Optional: **CodePipeline** ties it all together

---

## 🛠️ AWS Services Used

- **AWS CodeCommit** – Git repository  
- **AWS CodeBuild** – Build and test code; build/push Docker image  
- **Amazon ECR** – Docker image registry  
- **AWS CodeDeploy** – Deployment automation  
- **Amazon ECS (Fargate)** – Container orchestration  
- **CodePipeline** – Optional automation of pipeline steps  

---

## 🔐 Security Practices

- **IAM Roles** scoped for least privilege (e.g., CodeBuild role can only push to ECR)
- **ECS task roles** configured securely
- **S3 bucket** for artifacts has encryption and blocked public access
- **CodeCommit repo** access restricted to IAM users only

---

## 📸 Screenshots

Check `/screenshots/` for:
- CodePipeline execution details  
- CodeBuild logs  
- ECS service and task config  
- ECR repo with pushed image  

---

## 📚 Lessons Learned

- Built a production-style pipeline using only AWS services  
- Learned how CodeBuild integrates with ECR and ECS  
- Practiced setting up deployment strategies in ECS  
- Gained insight into managing buildspec.yml and task definition versions  

---

## ✍️ Author

Dom Pine – Cloud Security & AWS Learner  
[LinkedIn](https://linkedin.com) | [Portfolio](https://yourportfolio.com)

