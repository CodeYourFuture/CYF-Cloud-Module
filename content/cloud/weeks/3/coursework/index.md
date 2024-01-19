+++
title = 'coursework'
layout = 'coursework'
emoji= '📝'
menu_level = ['week']
weight = 3
coursework= 'Module-cloud'
coursework_filter= 'Week 3'
+++

## Dockerize CYF Hotel

The main aim of this week work is to become familiar with Docker Concepts and be able to use it to a base level. To achieve this, we'll keep working on our CYF Hotel.

## Prep

Ensure you complete the prep part and your Docker daemon is working correctly before continuin.

### Docker Backend

Start working on dockerising your application backend. Create a Dockerfile, set it up for node and replicate your setup and install steps that were manual so far in there. Iterate until you get it to run successfully as a Docker Container locally. Hint: Remember port forwarding!

Once successful, upload your created Docker Image to either your DockerHub account or (advanced) AWS's ECR. 
Once done, Update your EC2 instance to now run your backend as a container. Hint: You will need to set up Docker on the VM itself for this to work

### GitHub Pipelines

Once this is done and working fully, time to automate it - rework your Github Actions Workflow to test, build and upload your Docker image, and then deploy the new version to the EC2 machine.

### Local development (bonus)

This step is a bonus one, if you completed all previous steps and are not behind on the previous weeks.

Dockerise your Frontend, and have it run locally alongside via Docker with your backend. Can you get both to work correctly at the same time? Replicate the process for the database, and move it from your local instance to a local Docker Container (remember persistence via volumes).
In both cases, managed AWS services (S3 and RDS) give us a lot of advantages for Cloud Deployment, but lack support for local development, and Docker can help with that.

Imagine how you would automate, with a script, the process of rebuilding all 3 containers on changes, and restart/reconnect everything. Try to build it.

## Docker Compose - base orchestration (bonus)

Research Docker Compose, its syntax and a few examples. Think how it can help you orchestrate your 3 containers for local development, and then create a docker-compose file to use this tool to automatically build, start and network your containers. Find a way to specify dependencies, to ensure that the backend start initialising only when the database is up and running.

If you want, you can experiment with running all 3 components in EC2 via Docker compose, but keep it as an experiment. Think about some advantages and disadvantages of the 2 approaches (all in a docker-compose file inside a EC2 instance vs using multiple managed services such as S3 and RDS)