# AWS Infrastructure as Code Templates

Production-ready Terraform templates for common AWS infrastructure patterns. Built and tested on real deployments.

## Purpose

Reusable, modular IaC templates that provision AWS infrastructure consistently — from single-service deployments to multi-tier production environments.

## Structure

```
vpc/            # VPC, subnets, route tables, NAT gateway, security groups
ec2/            # EC2 instances, AMI selection, user-data scripts, auto scaling
rds/            # RDS MySQL/MariaDB, parameter groups, backups, read replicas
lambda/         # Lambda functions, IAM roles, triggers (S3, API GW, EventBridge)
s3/             # Buckets, lifecycle policies, versioning, CloudFront integration
modules/        # Reusable Terraform modules (shared across environments)
scripts/        # Helper scripts: init, plan, apply, destroy workflows
```

## Usage

```bash
cd vpc/
terraform init
terraform plan -var-file=terraform.tfvars
terraform apply
```

## Patterns Covered

- [ ] Three-tier VPC (public / private / data subnets)
- [ ] EC2 + RDS (standard web app stack)
- [ ] Serverless (Lambda + API Gateway + S3)
- [ ] Container deployment (EC2 + Docker)
- [ ] Static site (S3 + CloudFront + Route53)

## Requirements

- Terraform >= 1.5
- AWS CLI configured (`aws configure`)
- IAM user with programmatic access

## Status

Active development — Week 7-10 of 10-week portfolio sprint.
