+++
title = 'coursework'
layout = 'coursework'
emoji= '📝'
menu_level = ['week']
weight = 3
coursework= 'Module-cloud'
coursework_filter= 'Week 5'
+++

## Setup Scalability And Monitoring for CYF Hotel

This week, you'll focus on implementing scalability features and monitoring capabilities for the CYF Hotel project. Below are the specific tasks you'll work on:

### Setup EC2 Load Balancers

**Create EC2 Load Balancer**: In the AWS Management Console, set up a new EC2 Load Balancer.

**Configure Load Balancer**: Add rules to your Load Balancer to route traffic to your EC2 instances.

**Test Load Balancer**: Ensure that the Load Balancer is distributing traffic across multiple EC2 instances.

### Set High Availability for RDS

**Modify RDS Instance**: In the AWS RDS Dashboard, modify your existing RDS instance to include Multi-AZ deployments for MySQL, PostgreSQL, SQL Server, or Oracle.

### Enable CloudWatch Alarms for CYF Hotel

**Navigate to CloudWatch**: In the AWS Management Console, navigate to the CloudWatch service.

**Create CPU Utilization Alarm**: Set up an alarm to monitor the CPU utilization of your EC2 instances.

**Create RDS Read/Write Alarm**: Set up another alarm to monitor the Read and Write capacity of your RDS instance.

### Extra Task: Use CloudWatch Metrics to Create Dashboards

**Create Custom Dashboard**: Utilize CloudWatch Metrics to create a custom dashboard that shows metrics for both EC2 and RDS services.

By completing these tasks, you'll gain practical experience in implementing scalability and monitoring within AWS, essential for maintaining a healthy and efficient application.

### Extra Task: Use Terraform

**Terraform**: update the existing terraform files to add the previous steps in this coursework.
