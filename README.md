# 🏗️ Terraform Practice Configs

> A hands-on collection of Terraform configurations covering core AWS infrastructure concepts — from EC2 and VPCs to IAM, S3, Modules, Backends, and more.

---

## 👤 Author

**Muhammad Mubashar**
Junior DevSecOps / Cloud Infrastructure Engineer
🔗 [GitHub Profile](https://github.com/fsdmubashar)

---

## 📌 What is This Repo?

This repository contains **Terraform (IaC) practice configurations** built on AWS. Each folder is an independent mini-project covering a specific Terraform concept or AWS service. It is designed for learning and hands-on practice of real-world infrastructure provisioning.

> ⚠️ **Note:** This repo is forked from [paulgitrepo/mprashant-terraform-configs](https://github.com/paulgitrepo/mprashant-terraform-configs) and customized for personal learning.

---

## 🗂️ Folder Structure & What Each Does

| Folder | Description |
|---|---|
| `aws-ec2/` | Provision AWS EC2 instances using Terraform |
| `aws-s3/` | Create and manage S3 buckets with Terraform |
| `aws-vpc/` | Build a custom AWS VPC (subnets, route tables, IGW) |
| `aws-vpc-ec2-nginx/` | Full setup: VPC + EC2 + Nginx web server |
| `aws-IAM-management/` | Create IAM users, roles, and policies via Terraform |
| `proj-static-website/` | Deploy a static website on S3 with Terraform |
| `tf-variables/` | Practice Terraform input variables and outputs |
| `tf-functions/` | Use built-in Terraform functions (e.g. `length`, `join`, `lookup`) |
| `tf-operators-exps/` | Terraform expressions, operators, and conditionals |
| `tf-data-sources/` | Use `data` blocks to fetch existing AWS resources |
| `tf-backend/` | Configure remote state backend (S3 + DynamoDB locking) |
| `tf-cli-workspace/` | Manage multiple environments using Terraform workspaces |
| `tf-module-vpc/` | Use public registry VPC module (`terraform-aws-modules/vpc`) |
| `tf-own-module-VPC/` | Build and use a custom/local Terraform VPC module |
| `testing-local-module/` | Test locally written reusable Terraform modules |
| `tf-multi-resources/` | Provision multiple resources together in one config |
| `tf-test/` | Sandbox / experimental Terraform configurations |

---

## ⚙️ Prerequisites

Before using any configuration in this repo, make sure you have:

- [Terraform](https://developer.hashicorp.com/terraform/downloads) `>= 1.0` installed
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html) configured with valid credentials
- An AWS account with appropriate permissions

```bash
# Verify Terraform installation
terraform -version

# Verify AWS CLI and credentials
aws sts get-caller-identity
```

---

## 🚀 How to Use Any Configuration

Every folder follows the same Terraform workflow:

```bash
# Step 1: Go into any folder
cd aws-ec2

# Step 2: Initialize Terraform (download providers)
terraform init

# Step 3: Preview what will be created
terraform plan

# Step 4: Apply and provision resources
terraform apply

# Step 5: Destroy resources when done (avoid AWS charges!)
terraform destroy
```

---

## 🔐 AWS Credentials Setup

Make sure your AWS credentials are configured before running any config:

```bash
aws configure
# Enter: AWS Access Key ID
# Enter: AWS Secret Access Key
# Enter: Default region (e.g. us-east-1)
# Enter: Output format (json)
```

---

## 🧠 Key Concepts Covered

- **Terraform Basics** — providers, resources, variables, outputs
- **AWS Networking** — VPC, Subnets, Internet Gateway, Route Tables, Security Groups
- **Compute** — EC2 instances with user data scripts
- **Storage** — S3 bucket creation, static website hosting
- **IAM** — Users, Roles, Policies as code
- **Modules** — Public registry modules + custom local modules
- **State Management** — Remote backend with S3 + DynamoDB state locking
- **Workspaces** — Managing dev/staging/prod environments
- **Data Sources** — Referencing existing infrastructure
- **Functions & Expressions** — Dynamic configuration with Terraform HCL

---

## 📁 Languages Used

![HCL](https://img.shields.io/badge/HCL-94.5%25-blue)
![CSS](https://img.shields.io/badge/CSS-3.7%25-purple)
![HTML](https://img.shields.io/badge/HTML-1.8%25-orange)

---

## 📚 Learning Resources

- [Terraform Official Docs](https://developer.hashicorp.com/terraform/docs)
- [AWS Provider Registry](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)
- [Terraform Module Registry](https://registry.terraform.io/browse/modules)
- [Terraform Best Practices](https://www.terraform-best-practices.com/)

---

## ⚠️ Cost Warning

> Some configurations in this repo provision **billable AWS resources** (EC2, NAT Gateway, etc.).
> Always run `terraform destroy` after practice to avoid unexpected charges.

---

## 📝 License

This project is for **educational and practice purposes only**.
