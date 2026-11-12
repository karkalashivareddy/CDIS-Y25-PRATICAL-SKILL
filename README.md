# CDIS-Y25 Practical & Skill Records

![Course](https://img.shields.io/badge/Course-Cloud%20Infrastructure%20%26%20Services-0A66C2)
![Program](https://img.shields.io/badge/Program-B.Tech%20CSE-1F6FEB)
![Year](https://img.shields.io/badge/Academic%20Year-2026-2EA043)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange)

A structured record of the practicals and skills completed for the **Cloud Infrastructure and Services (CDIS)** course. This repository contains the documentation, step-by-step procedures, observations, and output evidence for each practical and skill performed during the academic session.

---

## Overview

The **Cloud Infrastructure and Services** course introduces the fundamental concepts of cloud computing, including cloud service models, deployment models, virtualization, storage, networking, and the provisioning of cloud resources. The practical sessions are designed to provide hands-on experience with industry-leading cloud platforms such as **Amazon Web Services (AWS)**.

Each practical and skill is documented in a standard record format containing:

- **Aim** — the objective of the experiment
- **Description** — the theoretical background and context
- **Steps** — the procedure followed to complete the experiment
- **Result** — the outcome of the experiment
- **Output** — screenshots and evidence of the resources provisioned

---

## Student Details

| Field | Details |
| :--- | :--- |
| **Name** | Karkala Shiva Reddy |
| **Roll Number** | 2520030105 |
| **Section** | 3 |
| **Program** | B.Tech. Computer Science and Engineering (CSE) |
| **Trimester** | 5 |
| **Course** | Cloud Infrastructure and Services |
| **Course Code** | 25CS2206E |
| **Academic Year** | 2026 |
| **Institution** | Department of CSE |

---

## Repository Structure

```text
CDIS-Y25-PRATICAL-SKILL/
│
├── Practical/
│   ├── Practical-1/
│   │   └── CDIS_Lab_Record_2520030105_Karkala_Shiva_Reddy.pdf
│   │
│   └── Practical-2/
│       └── CDIS_Lab_Record_2520030105_Karkala_Shiva_Reddy.pdf
│
├── Skill/
│   └── Skill-1/
│       └── CDIS_Skill_Record_2520030105_Karkala_Shiva_Reddy.pdf
│
├── .gitignore
└── README.md
```

---

## Practical Index

| No. | Practical Title | Document | Status |
| :---: | :--- | :--- | :---: |
| 1 | To create an AWS free tier account to provision the resources | [Lab Record](Practical/Practical-1/CDIS_Lab_Record_2520030105_Karkala_Shiva_Reddy.pdf) | ✅ Completed |
| 2 | Enabling MFA, creating a first Linux instance, and creating an S3 bucket with five uploaded objects | [Practical Record](Practical/Practical-2/CDIS_Lab_Record_2520030105_Karkala_Shiva_Reddy.pdf) | ✅ Completed |

> The index will be updated as additional practicals are completed and documented.

---

## Skill Index

| No. | Skill Title | Document | Status |
| :---: | :--- | :--- | :---: |
| 1 | Create an IAM user with programmatic access only, download the access key and secret key, and set up a billing alert for the account so that an email is received when the Free Tier limit is about to be crossed | [Skill Record](Skill/Skill-1/CDIS_Skill_Record_2520030105_Karkala_Shiva_Reddy.pdf) | ✅ Completed |

> The index will be updated as additional skills are completed and documented.

---

## Practical 1 — AWS Free Tier Account Setup

**Aim:** To create an AWS free tier account to provision the resources.

**Description:**
The AWS Free Tier allows new users to explore and use a wide range of AWS cloud services free of cost for a limited period. It includes *12-Months Free*, *Always Free*, and *Short-Term Trial* offers across services such as Amazon EC2, Amazon S3, Amazon RDS, AWS Lambda, Amazon DynamoDB, and Amazon SageMaker.

**Procedure Summary:**

1. Open the AWS website and start the account creation process.
2. Provide the account credentials and contact information.
3. Complete identity and payment verification.
4. Activate the Basic (Free) support plan.
5. Sign in to the AWS Management Console.
6. Provision and verify resources within the Free Tier limits.

**Outcome:**
An AWS free tier account was created successfully, and the required cloud resources were provisioned and verified through the AWS Management Console.

---

## Practical 2 — MFA, Linux Instance and S3 Bucket

**Aim:** To enable Multi-Factor Authentication (MFA) for secure access to the AWS account, create a first Linux instance in Amazon EC2 and connect to it, and create an S3 bucket and upload five objects with different file extensions.

**Description:**
Multi-Factor Authentication adds a second verification step to the user name and password. AWS supports passkeys and security keys, which use the device's fingerprint, face unlock or screen lock. Amazon EC2 provides resizable compute capacity in the cloud, and a Linux instance is launched from an Amazon Machine Image (AMI). The Amazon Linux 2023 AMI with the t3.micro instance type is free tier eligible. Amazon S3 is an object storage service in which data is stored as objects inside buckets, and Block Public Access keeps the bucket private.

**Procedure Summary:**

1. Open IAM security credentials and assign a passkey MFA device to the root account.
2. Search for EC2 and open the EC2 Dashboard.
3. Launch an Amazon Linux 2023 t3.micro instance named MYCOMPUTER with a new key pair and security group.
4. Connect to the instance using EC2 Instance Connect and run basic Linux commands.
5. Terminate the instance after verifying the commands.
6. Open Amazon S3 and create a bucket in the Europe (Stockholm) region with public access blocked.
7. Upload five files with different extensions (.pdf, .txt, .jpg, .csv and .docx).
8. Create a second bucket to understand unique bucket naming and confirm that both buckets are listed.

**Outcome:**
Multi-Factor Authentication was enabled for the AWS account using a passkey, a first Linux instance was launched, connected and terminated successfully, and an S3 bucket was created with five objects of different file extensions. A second bucket was also created to verify unique bucket naming.

---

## Skill 1 — IAM User with Programmatic Access and Billing Alert

**Aim:** Create an IAM user with programmatic access only, download the access key and secret key, and set up a billing alert for the account so that an email is received when the Free Tier limit is about to be crossed.

**Description:**
An IAM user is an identity created within an AWS account. Programmatic access allows the user to call AWS services through the AWS CLI, the AWS SDKs or direct API calls using an access key, without console access. An access key consists of an Access Key ID and a Secret Access Key, and the secret key can be viewed or downloaded only once at the time of creation. Since the account is a free tier account, AWS Budgets is used to set up a zero spend budget that sends an email notification whenever the spending exceeds $0.01, alerting the account owner before the free tier limit is crossed.

**Procedure Summary:**

1. Open the IAM console, choose IAM users and click Create user.
2. Enter the user name, keep console access unchecked (programmatic access only) and click Next.
3. Select Attach policies directly and attach the AdministratorAccess policy.
4. Review and create the user.
5. Open the user, go to Security credentials and click Create access key.
6. Select the Command Line Interface (CLI) use case and continue.
7. Download the access key and secret key as a CSV file.
8. Verify that the access key is listed with the status Active.
9. Search for billing and open Billing and Cost Management.
10. Go to Budgets and click Create budget.
11. Select the Zero spend budget template.
12. Enter the budget name and the email recipient, then create the budget.

**Outcome:**
An IAM user with programmatic access only was created successfully, the access key and secret access key were generated and downloaded, and a billing alert was set up using a zero spend budget so that an email is received when the spending is about to cross the free tier limit.

---

## Project Repository

The project work associated with this course is maintained separately:

- **CDIS-KLH-Y25-Project** — [https://github.com/karkalashivareddy/CDIS-KLH-Y25-Project](https://github.com/karkalashivareddy/CDIS-KLH-Y25-Project)

---

## Tools and Technologies

| Category | Tools / Services |
| :--- | :--- |
| **Cloud Platform** | Amazon Web Services (AWS) |
| **Core Services** | Amazon EC2, Amazon S3, Amazon RDS, AWS Lambda, Amazon DynamoDB, AWS IAM (MFA), AWS Budgets |
| **Console** | AWS Management Console, EC2 Instance Connect |
| **Documentation** | PDF (institutional practical and skill record format) |
| **Version Control** | Git and GitHub |

---

## How to Use This Repository

1. Clone the repository:

   ```bash
   git clone https://github.com/karkalashivareddy/CDIS-Y25-PRATICAL-SKILL.git
   ```

2. Navigate to the practical or skill folder you want to review.
3. Open the corresponding `.pdf` record using any standard PDF viewer.
4. Refer to the **Output** section of each record for the evidence.

---

## Notes

- Each record is prepared in the prescribed institutional format.
- Screenshots and outputs are included as proof of successful completion.
- Practicals and skills are added progressively as the course advances.
- Sensitive credentials such as passwords and secret access keys are never included in the records.

---

## Author

**Karkala Shiva Reddy**
B.Tech. CSE — Trimester 5
Roll Number: 2520030105
Section: 3

- GitHub: [@karkalashivareddy](https://github.com/karkalashivareddy)

---

*This repository is maintained for academic purposes as part of the CDIS course.*
