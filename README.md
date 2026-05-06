# ML App with Jenkins CI/CD

A simple machine learning web application demonstrating the use of **Jenkins for CI/CD automation**. The project focuses on building and running a Docker image automatically using a Jenkins pipeline.

## Overview

This project shows how Jenkins can be used to automate the build process of a containerized ML application.

- Train/load a basic ML model
- Serve predictions via a simple app (Flask)
- Build Docker image using Jenkins pipeline
- Run container automatically after build

## Tech Stack

Python, Flask (or similar), Docker, Jenkins

## Docker Usage (Manual)

Build image:
docker build -t ml-jenkins-app .

Run container:
docker run -p 5000:5000 ml-jenkins-app

Open in browser:
http://localhost:5000

## Jenkins Pipeline

Jenkins automates the Docker build process using a pipeline job.

Steps:
- Pull code from GitHub
- Install dependencies
- Build Docker image
- Run container (optional)
