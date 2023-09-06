+++
title = 'week-plan'
layout = 'week-plan'
emoji= '📝'
menu_level = ['week']
weight = 2
coursework= 'Module-cloud'
coursework_filter= 'Week 2'
+++

## Introduction to CI/CD Concepts

### What are CI and CD?

**CI**, or Continuous Integration, is a development practice where developers integrate code into a shared repository frequently. This usually happens multiple times a day and is complemented by automated tests.

**CD**, or Continuous Deployment/Delivery, takes the code changes from a repository, automatically builds and tests them, and then automatically deploys the tested code to a live service.

These practices make it easier to catch bugs earlier and make deployments faster and more reliable.

## Learning GitHub Actions Basics

### What are GitHub Actions?

GitHub Actions is an automation framework that runs in your GitHub repository. It can build, test, and deploy your code right from GitHub.

#### Key Components

**Workflows**: Orchestrates your CI/CD process.
**Jobs**: Sets of steps that execute sequentially.
**Steps**: Individual tasks within a job.
**Actions**: Pre-built steps that you can use in your jobs.

## Setting up a Simple Workflow

To set up a simple GitHub Actions workflow, navigate to your GitHub repository and then to the Actions tab. From there, you can create a new workflow.

Here's a basic example:

``` yaml
name: CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v2
```

This YAML file specifies a single job called build that runs on an ubuntu-latest runner machine. The job has a single step that uses actions/checkout@v2 to download the code from the GitHub repository.

## Adding Testing Stages

Testing is crucial in CI/CD pipelines. GitHub Actions can automatically run your tests every time someone pushes to your repository.

For example, if you're using Node.js and Jest for your tests:

``` yaml
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v2
    - name: Install Dependencies
      run: npm install
    - name: Run tests
      run: npm test
```

## Adding Deployment Stages

Once your code has been built and tested, you can deploy it automatically using GitHub Actions.

Here's a simplified example:

``` yaml
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
    - name: Deploy
      run: npm deploy
```

In this example, we use a custom command script for deploy. In your package.json you will have a section for scripts:

``` json
  "scripts": {
    "deploy": "echo this is a deploy",
  }
```

### Creating a Workflow with Multiple Jobs

In a real-world scenario, you often need multiple jobs to run different tasks in parallel or sequentially to speed up the process or manage dependencies. In this section, you'll learn how to set up a workflow with multiple jobs.

#### Example: npm test and Deployment

Here's an example YAML configuration file for a GitHub Actions workflow that has two jobs: one for running tests and another for deployment.

``` yaml
name: CI/CD Pipeline

on: [push]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v2
    - name: Install Dependencies
      run: npm install
    - name: Run tests
      run: npm test

  deploy:
    needs: test
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v2
    - name: Deploy
      run: npm deploy
```

Understanding the Workflow
**jobs**: Contains two job blocks: test and deploy.
**runs-on**: Specifies the type of runner that the job will run on.
**steps**: The sequence of tasks that will be executed in each job.
**needs**: This key in the deploy job specifies that it needs the test job to complete successfully before it starts.

By defining both jobs in the same YAML file, GitHub Actions will know to run them as part of the same workflow. The needs keyword ensures that the deploy job will only run if the test job completes successfully, adding a layer of protection against bugs making their way into production.

And that's how you set up a GitHub Actions workflow with multiple jobs. This allows you to make your CI/CD process more robust and maintainable.
