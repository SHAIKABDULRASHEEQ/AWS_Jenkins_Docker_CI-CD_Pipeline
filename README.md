# AWS Jenkins Docker CI/CD Pipeline

## Project Overview

Built an end-to-end CI/CD pipeline on AWS using Jenkins and Docker. Integrated GitHub with Jenkins to automate code checkout, Docker image build, and application deployment on an EC2 application server.

## Architecture

GitHub → Jenkins Server → Docker Build → Application Server → Running Container

## Tech Stack

- AWS EC2
- Jenkins
- Docker
- GitHub
- Linux
- Shell Scripting

## Key Features

- Jenkins pipeline automation
- GitHub source integration
- Docker image build and container deployment
- SSH-based remote deployment to application server
- Automated restart of updated containers

## CI/CD Flow

1. Developer pushes code to GitHub
2. Jenkins fetches latest source code
3. Docker image is built automatically
4. Image transferred to application server
5. Container deployed with latest version

## Important Files

- `Jenkinsfile`
- `Dockerfile`
- Application source code

## Sample Commands Used

```bash
docker build -t devops-app .
docker run -d -p 80:5000 devops-app
scp image.tar ec2-user@server:/home/ec2-user/
ssh ec2-user@server
