# Docker Containerized Application Deployment on AWS

## Project Overview
This project demonstrates how to build, containerize, and deploy a simple web application using Docker and AWS cloud services.

The application is deployed on an AWS EC2 instance using Docker and is also deployed using Amazon ECS with AWS Fargate.

## Technologies Used
- AWS EC2
- Docker
- Amazon ECR
- Amazon ECS
- AWS Fargate
- GitHub
- Nginx
- HTML

## Project Architecture

**Deployment 1: EC2 + Docker**

1. Launched an Ubuntu EC2 instance.
2. Installed Docker on the EC2 instance.
3. Created a simple HTML web application.
4. Configured Nginx to serve the application on port 8081.
5. Built a Docker image and ran the container.
6. Accessed the application using the EC2 public IP.

**Deployment 2: ECS + Fargate**

1. Created a private Amazon ECR repository.
2. Uploaded the Docker image to ECR.
3. Created an ECS cluster.
4. Created a Fargate task definition.
5. Configured an ECS service.
6. Enabled public IP access and configured port 8081.
7. Verified the application using the Fargate task's public IP.

## Docker Commands

Build the Docker image:

```bash
sudo docker build -t devops-internship-app .
```

Run the container:

```bash
sudo docker run -d -p 8081:8081 --name devops-container devops-internship-app
```

Check running containers:

```bash
sudo docker ps
```

Test the application:

```bash
curl http://localhost:8081
```

## Repository Structure

```text
devops-internship-docker/
├── Dockerfile
├── index.html
├── nginx.conf
└── README.md
```

## Deployment Result

Successfully deployed a Docker containerized web application on AWS EC2 and AWS ECS Fargate.

The application was accessible through a public IP address on port 8081.

## Learning Outcomes

- Understanding AWS EC2 infrastructure.
- Installing and working with Docker.
- Building and running Docker containers.
- Managing source code using GitHub.
- Uploading Docker images to Amazon ECR.
- Deploying containers using ECS and Fargate.
- Configuring networking and security groups in AWS.

## Author
GitHub: [Krishnapattar0608](https://github.com/Krishnapattar0608)
