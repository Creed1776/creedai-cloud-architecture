# Creed AI Cloud Architecture

Welcome to the official cloud architecture repo for Creed AI Solutions by Skavengaz Creed.

This project builds a scalable and secure AWS infrastructure using Terraform, automated by GitHub Actions.

## Features
- Custom VPC with public/private subnets
- EC2 with autoscaling
- S3 + CloudFront for static content
- GitHub Actions CI/CD
- IAM roles + policies for secured access

## Diagram
![VPC Architecture](architecture/vpc-diagram.png)
provider "aws" {
  region = var.region
}

resource "aws_vpc" "main" {
  cidr_block = "10.0.0.0/16"
  tags = {
    Name = "creedai-vpc"
  }
}
