+++
title = 'coursework'
layout = 'coursework'
emoji= '📝'
menu_level = ['week']
weight = 3
coursework= 'Module-cloud'
coursework_filter= 'Week 4'
+++

## Coursework: Infrastructure as Code for CYF Hotel

### Infrastructure as Code for CYF Hotel Frontend in S3

1. **Objective**: Use Terraform to deploy your CYF Hotel frontend to an S3 bucket.
2. **Steps**:
    - Write a Terraform configuration file (`main.tf`) to define the S3 bucket.
    - Include the necessary configurations like ACL, policy, and versioning.
    - Deploy the code to AWS.
3. **Outcome**: After running `terraform apply`, you should see the CYF Hotel frontend live on the S3 bucket URL.

### Infrastructure as Code for CYF Hotel Backend in EC2

1. **Objective**: Use Terraform to deploy your CYF Hotel backend to an EC2 instance.
2. **Steps**:
    - Write a Terraform configuration file (`main.tf`) to define the EC2 instance.
    - Include configurations for security groups, key pairs, and IAM roles if necessary.
    - Deploy the code to AWS.
3. **Outcome**: After running `terraform apply`, the backend should be running on an AWS EC2 instance accessible via its IP address.

### Infrastructure as Code for CYF Hotel Database in RDS

1. **Objective**: Use Terraform to deploy your CYF Hotel database to an RDS instance.
2. **Steps**:
    - Write a Terraform configuration file (`main.tf`) for the RDS database.
    - Include necessary configurations like database engine, version, and credentials.
    - Deploy the code to AWS.
3. **Outcome**: After running `terraform apply`, the database should be live and reachable on the RDS instance.

### Extra Exercise: Using Terraform Modules and Remote State

#### Objective

In this exercise, you will utilize a Terraform module to create a reusable configuration for S3 buckets. Additionally, you'll implement remote state management using an S3 bucket.

#### Steps

1. **Create a Terraform Module for S3 Buckets**
    - Create a new directory named `s3_module` and place a new Terraform file inside it, e.g., `main.tf`.
    - Define the Terraform code for an S3 bucket inside this file.

2. **Implement Remote State in S3**
    - In your main Terraform configuration (`main.tf`), configure the backend for remote state using S3.

3. **Initialize and Apply**
    - Initialize your Terraform project.
    - Apply the configuration to create the S3 bucket using the module and configure remote state.

#### Validation

- Confirm that the S3 bucket was created as expected.
- Check the S3 bucket where you store the remote state to ensure that the `terraform.tfstate` file is present.

#### References

- [Terraform Modules](https://developer.hashicorp.com/terraform/language/modules)
- [Terraform S3 Backend](https://developer.hashicorp.com/terraform/language/settings/backends/s3)
