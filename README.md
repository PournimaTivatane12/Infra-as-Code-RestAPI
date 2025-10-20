# Infra-as-Code-RestAPI

**A simple, production-minded DevOps project that deploys a Python REST API backed by MySQL. Infrastructure is created with Terraform on AWS. The application runs on an EC2 instance and connects to an RDS MySQL database. Jenkins provides CI/CD to build, test, and deploy the app. This README gives step-by-step instructions to reproduce the project locally and in AWS**

### 📚 Table of Contents

| Sr. No | Section Title                                | Sub Sections                                                                 |
|--------|---------------------------------------------|-------------------------------------------------------------------------------|
| 1      | Project Overview                             | -                                                                             |
| 2      | Architecture Diagram                         | -                                                                             |
| 3      | Components Used                              | -                                                                             |
| 4      | Prerequisites                                | -                                                                             |
| 5      | Setup Steps                                  | Prepare AWS and credentials <br> Provision infrastructure with Terraform <br> Configure RDS and security groups <br> Provision and configure EC2 (deploy app) <br> Application setup and database migration <br> CI/CD pipeline with Jenkins |
| 6      | Testing and Verification                     | -                                                                             |
| 7      | Cleanup                                      | -                                                                             |
| 8      | Security and Cost Notes                      | -                                                                             |
| 9      | Troubleshooting Tips                         | -                                                                             |
| 10     | Contributing and License                     | -                                                                             |



# 1 — Project overview

This project demonstrates a typical web application deployment flow:

-Infrastructure as code with Terraform to create VPC, subnets, security groups, EC2 instance, and RDS MySQL instance.

-Python REST API that performs CRUD against MySQL.

-Jenkins pipeline that pulls code, runs tests, builds a package, and deploys to EC2.

-Minimal production practices: environment variables, security groups, least privilege IAM role for EC2 or Terraform user, and proper cleanup scripts.

 # 2 — ARCHITECTURE 

<img width="763" height="426" alt="Screenshot 2025-10-17 185356" src="https://github.com/user-attachments/assets/8f593174-0a59-4d98-9524-920cd3f2546c" />

Web client -> REST API (running on EC2) -> MySQL on RDS
Terraform provisions EC2 and RDS. Jenkins orchestrates CI/CD.

# 3 — Components used

-AWS: VPC, Subnet, Internet Gateway, Route Tables, Security Groups, EC2 (Linux), RDS MySQL

-Terraform: for infrastructure

-Python: Flask or FastAPI for REST API

-MySQL client library (e.g. mysql-connector-python or pymysql)

-Jenkins: for CI/CD

-Git: source control

-(Optional) Nginx or Gunicorn for serving the Python app in production

-(Optional) Systemd for process management on EC2 or Docker if you prefer containers

# 4 — Prerequisites

-An AWS account with programmatic access. Ability to create EC2, RDS, IAM, VPC resources.

-Terraform installed (v1.x recommended).

-AWS CLI installed and configured.

-Jenkins server or Jenkins in Docker.

-Git, Python 3.8+ on local machine and EC2 AMI.

-Basic AWS IAM permissions for Terraform and Jenkins: create/update/delete EC2, RDS, VPC, security groups, and optionally IAM roles.

-A domain name is optional if you want DNS.


| Section                                    | Purpose                                                |
| ------------------------------------------ | ------------------------------------------------------ |
| **Project Features**                       | Quick bullet list of what the project does             |
| **Use Cases / Real-World Scenario**        | Explains where this project fits in real cloud systems |
| **Folder Structure**                       | Helps users understand your repo layout                |
| **Design Decisions**                       | Shows professional thinking behind tech choices        |
| **Future Improvements**                    | Shows you think like a DevOps engineer                 |
| **DevOps Practices Used**                  | Highlights skills clearly to recruiters                |
| **Monitoring + Logging Plan** *(optional)* | Adds a production-ready feel                           |
| **Why This Project Matters**               | Strong self-branding statement                         |

### ✅ Project Features

| Sr. No | Feature                                   | Description                                                                 |
|--------|-------------------------------------------|-----------------------------------------------------------------------------|
| 1      | Infrastructure as Code (IaC) using Terraform | Automates creation of AWS resources like EC2, RDS, and Security Groups       |
| 2      | REST API built with Python Flask          | Backend service exposes CRUD APIs for data operations                      |
| 3      | MySQL database hosted on AWS RDS          | Secure and scalable relational database hosted on AWS                      |
| 4      | Deployed on AWS EC2 Linux instance        | Application hosted on a cloud compute server                               |
| 5      | Jenkins CI/CD pipeline                    | Automates build, test, and deployment process                              |
| 6      | Secure architecture using AWS Security Groups | Restricts access and protects infrastructure                                 |
| 7      | Modular Terraform code                    | Reusable and maintainable Terraform module structure                       |
| 8      | Environment-based configuration           | Supports `.env` config for dev and production                              |
| 9      | CRUD application example                  | Implements Create, Read, Update, Delete operations                         |
| 10     | Git-based workflow                        | Uses Git and GitHub for source version control                             |

.
├── app/
│   ├── app.py
│   ├── requirements.txt
│   ├── config.py
│   └── db/
│       └── init_db.sql
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   ├── ec2.tf
│   ├── rds.tf
│   ├── vpc.tf
│   └── outputs.tf
├── Jenkinsfile
├── README.md
└── LICENSE









