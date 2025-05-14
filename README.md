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
<img src="https://sdmntprsouthcentralus.oaiusercontent.com/files/00000000-95d8-61f7-be2c-cc13b237d504/raw?se=2025-05-14T05%3A41%3A38Z&amp;sp=r&amp;sv=2024-08-04&amp;sr=b&amp;scid=00000000-0000-0000-0000-000000000000&amp;skoid=24a7dec3-38fc-4904-b888-8abe0855c442&amp;sktid=a48cca56-e6da-484e-a814-9c849652bcb3&amp;skt=2025-05-13T23%3A17%3A35Z&amp;ske=2025-05-14T23%3A17%3A35Z&amp;sks=b&amp;skv=2024-08-04&amp;sig=gVee8x47eZDTJadsJMeqRRjB818/83OUT1u3PYIcezU%3D"/>![image](https://github.com/user-attachments/assets/3a60cf57-a369-4d05-8cc8-8bbd71e9e5cb)
