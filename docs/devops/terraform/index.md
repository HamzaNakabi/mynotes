---
title: Terraform
tags:
  - devops
  - terraform
  - iac
---

# Terraform Notes

Infrastructure as Code with Terraform.

## Topics

- [ ] Core concepts
- [ ] State management
- [ ] Modules
- [ ] Workspaces
- [ ] Provider configuration
- [ ] Best practices

---

## Quick Reference

### Commands

```bash
# Initialize
terraform init

# Plan changes
terraform plan

# Apply changes
terraform apply

# Destroy resources
terraform destroy

# Format code
terraform fmt

# Validate configuration
terraform validate

# Show state
terraform state list
terraform state show <resource>
```

### Basic Example

```hcl
# Provider configuration
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }

  backend "s3" {
    bucket = "my-terraform-state"
    key    = "state/terraform.tfstate"
    region = "us-east-1"
  }
}

provider "aws" {
  region = var.aws_region
}

# Variables
variable "aws_region" {
  default = "us-east-1"
}

variable "environment" {
  type = string
}

# Resources
resource "aws_instance" "web" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t3.micro"

  tags = {
    Name        = "web-server"
    Environment = var.environment
  }
}

# Outputs
output "instance_ip" {
  value = aws_instance.web.public_ip
}
```

---

!!! warning "State Management"
    Always use remote state storage for team environments. Never commit `.tfstate` files to version control.
