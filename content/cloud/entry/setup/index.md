+++
title = 'setup'
layout = 'setup'
emoji= '📝'
menu_level = ['week']
weight = 2
coursework= 'Module-cloud'
coursework_filter= 'entry'
+++

## Setup

### 1. Ensure you have a project to deploy

You must already have a project (e.g. CYF Hotel project, Full Stack Assessment) which has

- A Frontend (e.g. a React App)
- A Backend (e.g. an Express App)
- A Database (e.g. a Postgres or MySql or MongoDB Database)
- We recommend using the "CYF Hotel" project from the course but you are welcome to use any project you like. This could be your final project from the Full Stack course or a project you've built in your own time.

You may already have this project deployed to a public hosting such as Render or Netlify. If you do, great - you're ready to go!

If you do not have a project, please speak to your teacher or the module leader.

### 2. Setup AWS Account

Before starting this course, it's essential to prepare by setting up some tools and services that we'll be using throughout the course. Follow these steps:

1. **Sign Up for AWS**: If you don't already have an AWS account, go to [AWS Home](https://aws.amazon.com/) and click on "Create an AWS Account."
2. **Complete Signup**: Follow the on-screen instructions. You'll need to provide a credit card for verification, but most of the services we'll be using fall under the AWS Free Tier.

#### 2.1 Implement MFA Authentication

To keep your account secure, we recommend setting up Multi-Factor Authentication (MFA). This will require you to enter a code from your phone or other device when logging in to AWS.

1. **Login to AWS Console**: After your account is set up, log in to the [AWS Management Console](https://aws.amazon.com/console/).
2. **Navigate to IAM**: In the AWS Console, find and click on "Services," then select "IAM" under Security, Identity, & Compliance.
3. **Set Up MFA**: In IAM, navigate to the "Dashboard," then click on "Activate MFA on your root account" and follow the instructions to set up Multi-Factor Authentication (MFA).

#### 2.2 Setup Budget Alerts

Finally, we recommend setting up budget alerts to monitor your AWS spending. This will help you avoid any unexpected charges.

1. **Navigate to AWS Budgets**: From the AWS Console, find and click on "Services," then select "Budgets" under Management & Governance.
2. **Create Budget**: Follow the prompts to create a budget, defining the cost or usage thresholds you want to track.
3. **Set Alerts**: While setting up the budget, you will have the option to configure alerts based on your budget thresholds. This way, you'll receive notifications if your spending or usage crosses the specified limits.
