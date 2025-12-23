---
title: AWS
tags:
  - cloud
  - aws
---

# AWS Notes

Amazon Web Services documentation and notes.

## Services

### Compute

- [ ] EC2
- [ ] Lambda
- [ ] ECS / EKS
- [ ] Fargate

### Storage

- [ ] S3
- [ ] EBS
- [ ] EFS
- [ ] Glacier

### Database

- [ ] RDS
- [ ] DynamoDB
- [ ] ElastiCache
- [ ] Redshift

### Networking

- [ ] VPC
- [ ] Route 53
- [ ] CloudFront
- [ ] API Gateway

### Security

- [ ] IAM
- [ ] KMS
- [ ] Secrets Manager
- [ ] Security Hub

---

## Useful Commands

```bash
# Configure AWS CLI
aws configure

# List S3 buckets
aws s3 ls

# Describe EC2 instances
aws ec2 describe-instances

# Get caller identity
aws sts get-caller-identity
```

---

!!! tip "Pro Tip"
    Use AWS CLI profiles for managing multiple accounts:
    ```bash
    aws configure --profile myprofile
    aws s3 ls --profile myprofile
    ```
