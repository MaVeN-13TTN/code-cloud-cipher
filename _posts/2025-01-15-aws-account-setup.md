---
layout: post
title: "Setting Up Your AWS Account: A Beginner's Guide"
date: 2025-01-15
categories: aws cloud security
tags: [aws, cloud computing, devops, security]
---

## 🚀 Introduction
Amazon Web Services (AWS) is a leading cloud platform offering scalable and secure infrastructure solutions. If you're new to AWS, this guide will walk you through setting up your account properly.

---

## 🔹 Step 1: Create an AWS Account
1. Visit [AWS Sign-Up](https://aws.amazon.com/) and click **"Create an AWS Account."**
2. Enter your **email address**, set a **password**, and choose an **AWS account name**.
3. Provide **billing details** (a valid credit/debit card is required, but AWS Free Tier is available).
4. Complete **identity verification** via phone or text message.
5. Select a **support plan** (choose "Basic" for free).

---

## 🔹 Step 2: Secure Your AWS Account
🔒 Security is crucial! Follow these steps to protect your account:
- **Enable MFA (Multi-Factor Authentication):**
  - Go to **AWS Management Console** → **IAM** → **Users** → **Security Credentials**.
  - Activate **MFA** (Google Authenticator recommended).
- **Create an IAM User for Daily Use:**
  - Never use the **root user** for regular tasks!
  - Create a new IAM user with **AdministratorAccess**.
  - Generate and store **Access Key ID** and **Secret Access Key** securely.
- **Set Up Billing Alerts:**
  - Navigate to **AWS Budgets** → Create a budget to monitor spending.

---

## 🔹 Step 3: Configure AWS CLI (Optional but Recommended)
The **AWS CLI** allows you to interact with AWS services from your terminal.

1. Install AWS CLI:
   - **Linux/macOS:**  
     ```bash
     curl "https://awscli.amazonaws.com/AWSCLIV2.pkg" -o "AWSCLIV2.pkg"
     sudo installer -pkg AWSCLIV2.pkg -target /
     ```
   - **Windows:** Download from [AWS CLI Official Page](https://aws.amazon.com/cli/).

2. Configure AWS CLI:
   ```bash
   aws configure
