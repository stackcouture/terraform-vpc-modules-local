# Terraform VPC Modules for AWS

## Overview

This project provides reusable Terraform modules to automate the creation and management of AWS VPC resources. It includes modules for:

- **VPC**: Creates a Virtual Private Cloud (VPC) in AWS with customizable CIDR blocks and tags.
- **Subnets**: Defines both public and private subnets, placing them in different availability zones for high availability.
- **Security Groups**: Sets up customizable security groups for controlling inbound and outbound traffic to resources.
- **EC2 Instances**: Provisions EC2 instances within the VPC, using your defined subnets and security groups.
- **NAT Gateway**: Deploys a NAT Gateway in a public subnet, allowing instances in private subnets to access the internet.
- **Route Tables**: Configures route tables for routing traffic between subnets and out to the internet via the Internet Gateway or NAT Gateway.

## Features

- **Modular design**: Easy customization to fit your specific requirements.
- **Public and Private Subnets**: Supports both public and private subnets for flexible networking configurations.
- **Automated provisioning**: Fully automated provisioning of AWS resources using Terraform.

## Prerequisites

Before using this project, ensure that you have the following prerequisites:

- **Terraform**: Ensure you have Terraform installed. You can download it from the official Terraform website: [https://www.terraform.io/downloads.html](https://www.terraform.io/downloads.html).
- **AWS Account**: You must have an active AWS account with the necessary IAM permissions to provision the required resources.

## Getting Started

Follow the steps below to get started with provisioning the VPC infrastructure.

## 1. Clone the Repository

  Clone the repository to your local machine:
  git clone https://github.com/stackcouture/terraform-vpc-modules-local.git

## 2. Navigate to the Module Directory
    
    Change into the project directory:
    cd terraform-vpc-modules-local

## 3. Modify the Variables
  Customize the configuration by modifying the terraform.tfvars file to define your desired VPC, subnet, and instance parameters.

  Example:
  vpc_cidr_block = "10.0.0.0/16"
  instance_type  = "t2.micro"
  az_name        = "us-west-2a"

## 4. Initialize Terraform
  Initialize Terraform to install the necessary providers and modules:
  terraform init

## 5. Apply the Configuration

  Once initialization is complete, you can apply the configuration to provision the resources:
  terraform apply
  You will be prompted to confirm the execution by typing yes.

## 6. Clean Up (Optional)

  To remove all the resources you’ve provisioned, you can use the following command:
  terraform destroy

## Resources

This project uses the following AWS resources:

- **VPC**: A Virtual Private Cloud to isolate your network.
- **Subnets**: Public and private subnets for deploying EC2 instances.
- **Security Groups**: Customizable security groups for controlling traffic.
- **EC2 Instances**: Provisions EC2 instances for hosting your applications.
- **NAT Gateway**: Allows instances in private subnets to access the internet.
- **Route Tables**: Manages routing for traffic across the VPC.

Contributing
If you’d like to contribute to this project, feel free to fork the repository, create a branch, and submit a pull request with your changes. We welcome all improvements and suggestions.

Disclaimer
This project is designed for educational purposes and may need further customization based on the specific requirements of your AWS infrastructure.

