This project demonstrates deploying a simple Node.js "Hello World" application to an AWS ECS Fargate cluster using a CI/CD pipeline.

Technology Stack:

Node.js
Docker
AWS Services:
Amazon ECR (EC2 Container Registry)
AWS CodeBuild
Amazon ECS Fargate
Getting Started

This are the few things required for the project-

Git version control installed
Docker installed and running
An AWS account with appropriate permissions
Project Structure:

This project uses the following files:

index.js: The Node.js application code
Dockerfile: Instructions for building a Docker image
buildspec.yml: Configuration for the AWS CodeBuild project
