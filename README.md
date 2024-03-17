Node.js Hello World Application Deployment on AWS ECS Fargate


This repository contains the necessary steps and files to deploy a simple Node.js "Hello World" application to an AWS ECS Fargate cluster using a CI/CD pipeline. Below are the steps to set up and deploy the application:

Preparation_

GitHub Repository Setup

Create a new public or private repository on GitHub.

Initialize a README.md file explaining the project and CI/CD setup.

Implement a branching strategy.

Node.js Application

Create a basic Node.js application with an index.js file containing the provided code.

Save the file as index.js.

Dockerfile Creation_

Create a Dockerfile in the project root with the provided content.

Save the Dockerfile in the project root directory.

AWS Setup_

IAM User Setup

Create a new IAM user named devops-user with programmatic access.

Attach the "AmazonEC2ContainerRegistryPowerUser" policy to allow ECR access.

ECR Repository Creation

In the Amazon ECR service, create a new repository named hello-world-app.

ECS Cluster Setup_

In the Amazon ECS service, create a new cluster named cicd-cluster.

Leave the cluster configuration with default settings for now.

CodeBuild Project Setup_

Build Project Creation

In the AWS CodeBuild service, create a new build project named hello-world-build.

Source Provider Configuration

Choose "GitHub" as the source provider and connect your GitHub repository.

Specify the build spec file path as buildspec.yml in the root of your repository.

Environment Variables

Define two environment variables:

AWS_DEFAULT_REGION: Set the value to ap-south-1 (Mumbai region).

ECR_REPO_URI: This will be dynamically populated during pipeline execution.

Build Spec Configuration_

Create a buildspec.yml file in your project root.
