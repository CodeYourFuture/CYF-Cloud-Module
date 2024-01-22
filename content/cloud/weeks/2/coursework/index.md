+++
title = 'coursework'
layout = 'coursework'
emoji= '📝'
menu_level = ['week']
weight = 3
coursework= 'Module-cloud'
coursework_filter= 'Week 2'
+++

## Setup Github Actions for CYF Hotel Frontend deployments to S3

Create GitHub Actions Workflow File: In your CYF Hotel repository, create a new YAML file under the .github/workflows directory. Name it something relevant, like frontend-s3-deploy.yml.

Configure AWS Credentials: Utilize GitHub Secrets to securely store your AWS credentials. These secrets will be used in the GitHub Actions workflow to authenticate against AWS.

Write S3 Deployment Steps: In the YAML file, define the steps to install AWS CLI, configure AWS credentials, and sync your build folder to your S3 bucket.

Test the Workflow: Push a change to your repository or manually run the workflow from the GitHub Actions tab to verify that the S3 deployment works as expected.

## Setup Github Actions for CYF Hotel Backend deployments to EC2

Create GitHub Actions Workflow File: Similar to the frontend, create a new YAML file in your CYF Hotel repository under .github/workflows, and name it appropriately, like backend-ec2-deploy.yml.

Configure AWS and SSH Credentials: Store your AWS and SSH credentials securely using GitHub Secrets. These will be used to authenticate and connect to your EC2 instance.

Write EC2 Deployment Steps: Outline the steps in the YAML file for SSHing into your EC2 instance, pulling the latest code, and restarting your backend service.

Test the Workflow: Like with the frontend, push a change to your repository or manually trigger the workflow from GitHub Actions to ensure that your backend is successfully deployed to the EC2 instance.
