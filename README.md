# Terraform CI/CD Pipeline with GitHub Actions

A production-ready CI/CD pipeline for Terraform using GitHub Actions, built from scratch. Instead of a basic demo, this project implements a workflow that follows real-world DevOps best practices — including separate Plan and Apply stages, pull request validation, manual approvals, remote state management, and secure AWS authentication.

By the end of this setup, you'll have a CI/CD pipeline suitable for production environments.

## 🚀 What You'll Build

- Production-ready Terraform workflow
- GitHub Actions CI/CD pipeline
- PR validation workflow with automatic:
  - `terraform fmt`
  - `terraform init`
  - `terraform validate`
  - `terraform plan`
- Plan artifact upload
- PR plan comments
- Manual approval before apply
- `terraform apply` after merge
- Remote state using S3
- State locking
- AWS IAM roles & GitHub OIDC authentication
- Environment protection rules
- Secure GitHub secrets
- Production DevOps best practices

## 🛠 Tech Stack

- Terraform
- GitHub Actions
- AWS IAM
- S3 Backend
- GitHub OIDC
- YAML

## 📚 Who This Is For

- DevOps Engineers
- Cloud Engineers
- Platform Engineers
- Terraform Beginners
- Students preparing for DevOps interviews
- Anyone learning Infrastructure as Code (IaC)

If you're serious about learning Terraform and DevOps, this production-grade pipeline follows the same style of workflow used by many engineering teams to safely deploy infrastructure.

## Getting Started

### Prerequisites

- [Terraform](https://developer.hashicorp.com/terraform/downloads) installed locally
- [AWS CLI](https://aws.amazon.com/cli/) installed and configured
- An AWS account with an IAM user/role that has permissions to manage the required resources
- A GitHub repository with Actions enabled

### Setup

1. Clone this repository
2. Configure your AWS credentials (`aws configure`)
3. Update `provider.tf` with your desired AWS region
4. Update the S3 backend configuration in `provider.tf` with your state bucket details
5. Run `terraform init` to initialize the working directory
6. Run `terraform plan` to preview changes
7. Run `terraform apply` to provision infrastructure

## Project Structure

```
.
├── provider.tf          # Terraform and AWS provider configuration, S3 backend
├── s3.tf                 # S3 bucket resources (e.g. remote state bucket)
├── .github/
│   └── workflows/         # GitHub Actions CI/CD workflows
└── README.md
```

## License

Add your license of choice here.
