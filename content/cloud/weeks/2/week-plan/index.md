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

#### Exercise: Review a github action from previous coursework

Github Actions have been present in the course, now we are going to take a look at them and review them.

Back in Javascript 1 Week 1, we can see an existing workflow for mandatory tests: <https://github.com/CodeYourFuture/JavaScript-Core-1-Coursework-Week1/blob/master/.github/workflows/mandatory-tests.yml>

You should have completed the Coursework for Javascript 1 Week 1, this exercise is for you to find your pull request and see the Github Action workflow. Go to <https://github.com/CodeYourFuture/JavaScript-Core-1-Coursework-Week1> to find your Pull Request or go directly to the Actions <https://github.com/CodeYourFuture/JavaScript-Core-1-Coursework-Week1/actions> to find your workflow run.

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
      uses: actions/checkout@v3
```

This YAML file specifies a single job called build that runs on an ubuntu-latest runner machine. The job has a single step that uses actions/checkout@v3 to download the code from the GitHub repository.

For more information on Github Actions Syntax refer to their documentation: <https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions>

## Adding Testing Stages

Testing is crucial in CI/CD pipelines. GitHub Actions can automatically run your tests every time someone pushes to your repository.

For example, if you're using Node.js and Jest for your tests:

``` yaml
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v3
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
      uses: actions/checkout@v3
    - name: Install Dependencies
      run: npm install
    - name: Run tests
      run: npm test

  deploy:
    needs: test
    runs-on: ubuntu-latest
    steps:
    - name: Checkout code
      uses: actions/checkout@v3
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

### Environment Variables and Secrets

In any development workflow, especially one that involves deployments, it's common to have configuration settings that should not be hard-coded in the codebase. This includes API keys, database URLs, and other sensitive information. GitHub Actions allows the use of environment variables and secrets to manage these configurations securely.

#### Github Environment Variables

Environment variables are key-value pairs that you can create and modify as part of your workflow. They can be accessed in your GitHub Actions YAML file via env context. For example, to set a Node.js environment, you can do:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    env:
      NODE_ENV: production
```

And then use it in a script like this:

```yaml
    - name: Using Environment Variable
      run: echo Node environment is ${{ env.NODE_ENV }}
```

#### Github Secrets

Secrets are similar to environment variables but are encrypted and only exposed to selected actions, adding an extra layer of security. They are ideal for storing sensitive data like passwords and API keys.

You can add secrets via GitHub by navigating to your repository, then clicking on *Settings* -> *Secrets* -> *New Repository Secret*. Enter the secret's name and value, and it will be encrypted and stored securely.

To use a secret, you refer to it using secrets context in your YAML file like this:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - name: Accessing secret
      run: echo Accessing secret ${{ secrets.MY_SECRET }}
```

In the example above, MY_SECRET would be replaced by the actual secret's name you've stored in the GitHub repository.

For more information about environment variable refer to their documentation: <https://docs.github.com/en/actions/learn-github-actions/variables> and for information about secrets refer to: <https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions>
