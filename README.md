# Employee DevOps Project

## Overview

A containerized Employee Management application demonstrating
application development, Docker containerization, and CI automation
using GitHub Actions.

## Tech Stack

- Python
- Flask
- Docker
- GitHub Actions
- AWS EC2

## Project Structure

employee-devops-project/
├── .github/workflows/deploy.yml
├── app/app.py
├── Dockerfile
├── requirements.txt
└── README.md

## Application

The application provides an Employee Management interface/API
implemented using Python and Flask.

## Docker

Build the image:

docker build -t employee-app .

Run the application:

docker run -d -p 5000:5000 --name employee-app-container employee-app

The application can then be accessed locally on port 5000.

## CI Workflow

Every push to the `main` branch triggers GitHub Actions.

Workflow:

GitHub Push
    ↓
Checkout Code
    ↓
Set up Python
    ↓
Install Dependencies
    ↓
Build Docker Image
    ↓
Success

## AWS Deployment

The application was previously deployed to an AWS EC2 instance
for project demonstration.

The EC2 instance was decommissioned after project completion.
The current GitHub Actions workflow performs application validation
and Docker image building without deploying to EC2.

## Current Status

- Source code maintained in GitHub
- Docker image builds successfully
- GitHub Actions workflow passes successfully
- AWS EC2 deployment has been decommissioned after completion

## How to Run Locally

Clone the repository:

git clone <repository-url>

cd employee-devops-project

Install dependencies:

pip install -r requirements.txt

Run the application:

python app/app.py

Or run using Docker:

docker build -t employee-app .
docker run -d -p 5000:5000 employee-app

## Author

Shital Dhaval
