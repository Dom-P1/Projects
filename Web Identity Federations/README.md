# 🔐 AWS Serverless App with Web Identity Federation

A serverless AWS application that uses **Web Identity Federation** to allow users to authenticate using a third-party identity provider (Google, Facebook, or Amazon) and interact with AWS resources securely via temporary credentials.

---

## 📘 Overview

**Problem:** Users need secure, short-term access to AWS resources without managing long-term credentials.

**Solution:** This project uses Web Identity Federation to allow users to log in with Google or Facebook, exchange the token with AWS STS, and access S3 or DynamoDB with temporary credentials.

---

## 🏗️ Architecture

![Architecture Diagram](architecture.png)

### Flow Summary:
- User logs in with Google/Facebook → receives token
- Token is exchanged with AWS STS via an IAM Role for temporary credentials
- Credentials are scoped to allow limited access (e.g., upload to S3)
- Optional: Lambda + API Gateway can be used for extra logic

---

## 🛠️ AWS Services Used

- **STS (Security Token Service)** – To generate temporary credentials
- **IAM Roles** – With trust policies for federated identities
- **S3 / DynamoDB** – Accessed using temporary creds
- **API Gateway + Lambda (optional)** – For handling secure API calls

---

## 🔐 Security Practices

- Web Identity Federation configured with **Google/Facebook**
- IAM trust policy allows `AssumeRoleWithWebIdentity`
- IAM policy limits what temporary credentials can do (e.g., `s3:PutObject` only)
- S3 buckets block public access, SSE enabled

---

## 📸 Screenshots

Find screenshots of AWS Console setup in the `/screenshots` folder:
- IAM Role trust relationship
- STS configuration
- Test token from Google/Facebook

---

## 📚 Lessons Learned

- Learned how to configure Web Identity Federation with STS
- Understood temporary credential lifecycle and session duration
- Practiced writing trust policies and permission boundaries

---

## ✍️ Author

Dom Pine – Cloud Security & AWS Learner  
[LinkedIn](https://linkedin.com) | [Portfolio](https://yourportfolio.com)
