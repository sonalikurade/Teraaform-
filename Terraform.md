# Title: Automating AWS Infrastructure with Terraform: User Creation, Deletion, EC2, S3, and VPC Creation

## Introduction:

Terraform is an infrastructure-as-code tool that allows you to manage and provision cloud resources in a predictable and efficient manner. In this blog post, we will explore how to use Terraform to automate AWS infrastructure, including user creation and deletion, EC2 instances, S3 buckets, and VPC configuration.

### User Creation and Deletion:

To create and manage AWS users with Terraform, use the aws_iam_user resource. Here's an example:

terraform
resource "aws_iam_user" "example" {
name = "example-user"
}

To delete a user, simply remove the resource block from your Terraform configuration file.

## EC2 Instances:

To create an EC2 instance with Terraform, use the aws_instance resource. Here's an example:

terraform
resource "aws_instance" "example" {
ami           = "ami-abc123"
instance_type = "t2.micro"
}

## S3 Buckets:

To create an S3 bucket with Terraform, use the aws_s3_bucket resource. Here's an example:

terraform
resource "aws_s3_bucket" "example" {
bucket = "example-bucket"
acl    = "private"
}

## VPC Configuration:

To create a VPC with Terraform, use the aws_vpc resource. Here's an example:

terraform
resource "aws_vpc" "example" {
cidr_block = "10.0.0.0/16"
}

### Conclusion:

Terraform provides a powerful way to automate AWS infrastructure management. By using Terraform, you can version control your infrastructure, reduce errors, and improve efficiency.