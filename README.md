# terraform-aws

# Infrastructure Deployment with Terraform

This repository contains Terraform code to deploy the following infrastructure components:

1. VPC
2. EC2 Instances
3. Security Groups
4. S3 Bucket
5. Application Load Balancer (ALB)
6. Route 53 (optional)
7. RDS (Relational Database Service)
8. RabbitMQ (optional)
9. IAM User

## Prerequisites

Before deploying the infrastructure, ensure that you have the following prerequisites:

- Terraform installed on your local machine
- AWS account credentials configured
- Proper access permissions to create and manage the required resources

## Directory Structure

The Terraform code is organized into separate files based on the infrastructure components:

- `vpc.tf`: Defines the VPC, subnets (public and private), route tables, subnet associations, internet gateway, NAT gateway.
- `ec2.tf`: Configures the EC2 instances.
- `sg.tf`: Defines the security groups with specific ingress and egress rules.
- `s3.tf`: Creates an S3 bucket.
- `alb.tf`: Sets up the Application Load Balancer (ALB) with target groups and listeners.
- `rds.tf`: Creates the RDS instance, subnet group, and database.
- Other necessary files for variables (`var.tf`) and outputs (`output.tf`).

## Usage

To deploy the infrastructure, follow these steps:
1. Initialize the Terraform configuration by running the following command:
terraform init

2. Review and modify the variables in the `var.tf` file according to your requirements.

3. Run the following command to preview the changes that will be applied:
terraform plan

4. If the plan looks good, apply the changes by running the following command:
terraform apply

Confirm the changes when prompted.

5. Wait for the infrastructure deployment to complete.

## Cleaning Up

To destroy the deployed infrastructure and clean up resources, run the following command:
terraform destroy

Confirm the destruction when prompted.

## Contributions
Contributions to this Terraform code are welcome. Feel free to submit any issues or pull requests if you find any improvements or fixes.


