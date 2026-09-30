# 🚀 Employee Management System — AWS DevOps Project

A hands-on DevOps project demonstrating containerization, cloud deployment, CI/CD automation, reverse proxy configuration, and infrastructure monitoring using AWS and open-source DevOps tools.

---

## 📌 Project Overview

The **Employee Management System** is a Python Flask web application containerized using Docker and deployed on an AWS EC2 instance.

The project implements:

- Docker-based application deployment
- Automated CI/CD pipeline using GitHub Actions
- Nginx reverse proxy configuration
- Prometheus monitoring
- Node Exporter system metrics
- Grafana dashboards

This project was built and tested as a practical AWS DevOps implementation.

---

# 🏗️ Architecture

## Application Deployment Flow

```text
Developer
    |
    | git push
    v
GitHub Repository
    |
    v
GitHub Actions
    |
    | SSH
    v
AWS EC2 (Ubuntu)
    |
    v
Docker Container
    |
    v
Nginx Reverse Proxy
    |
    v
Flask Application

Monitoring Architecture
AWS EC2
   |
   v
Node Exporter
   |
   v
Prometheus
   |
   v
Grafana Dashboard

🛠️ Technology Stack
Technology	Purpose
Python	Application Development
Flask	Web Framework
Docker	Containerization
AWS EC2	Cloud Server
Ubuntu	Operating System
Git	Version Control
GitHub	Source Code Management
GitHub Actions	CI/CD Automation
Nginx	Reverse Proxy
Prometheus	Monitoring
Node Exporter	System Metrics
Grafana	Dashboard Visualization

✨ Features
Application
Python Flask web application

Employee Management System interface

Dockerized application

Runs on port 5000

DevOps
Git-based workflow

Docker containerization

Automated CI/CD deployment

AWS EC2 deployment

Nginx reverse proxy

Monitoring
Prometheus metrics collection

Node Exporter integration

Grafana dashboards

CPU monitoring

Memory monitoring

Disk monitoring

Network monitoring

System uptime monitoring

🔄 CI/CD Pipeline
GitHub Actions automatically deploys the application whenever changes are pushed to the main branch.

Developer
    |
    | git push
    v
GitHub Repository
    |
    v
GitHub Actions
    |
    +-- Checkout Code
    |
    +-- Build Docker Image
    |
    +-- Connect to EC2 using SSH
    |
    +-- Pull Latest Code
    |
    +-- Stop Existing Container
    |
    +-- Remove Old Container
    |
    +-- Start New Container

🐳 Docker Setup
Build Image
docker build -t employee-app .

Run Container
docker run -d \
-p 5000:5000 \
--name employee-app-container \
employee-app

Check Container
docker ps

🌐 Nginx Configuration
Nginx is used as a reverse proxy between users and the Flask application.

Client
  |
  v
Nginx :80
  |
  v
Flask Application :5000

📈 Monitoring Stack
Prometheus
Prometheus collects metrics from EC2 through Node Exporter.

Target:

localhost:9100

Node Exporter
Collects:

CPU usage

Memory usage

Disk usage

Network traffic

Load average

System uptime

Grafana
Grafana connects with Prometheus and displays monitoring dashboards.

📁 Project Structure
employee-devops-project/

├── .github/
│   └── workflows/
│       └── deploy.yml
│
├── app/
│   └── app.py
│
├── Dockerfile
├── requirements.txt
└── README.md

🚀 Application Setup
Clone Repository
git clone https://github.com/shitaldhaval2004/employee-devops-project.git

cd employee-devops-project

Install Dependencies
pip install -r requirements.txt

Run Application
python app/app.py

Application:

http://localhost:5000

🔐 GitHub Actions Secrets
Sensitive EC2 details are stored securely using GitHub Secrets.

Required secrets:

EC2_HOST
EC2_USERNAME
EC2_SSH_KEY

🔒 Security Practices
SSH private keys are not committed to GitHub

Secrets are stored using GitHub Actions Secrets

AWS resources were used only for project implementation and testing

Cloud resources were removed after completion to avoid unnecessary costs

🧪 Deployment Testing
Deployment flow:

git push
    |
    v
GitHub Actions
    |
    v
Docker Build
    |
    v
Container Updated
    |
    v
Application Updated

📊 Monitoring Verification
Monitoring flow:

Node Exporter
      |
      v
Prometheus
      |
      v
Grafana

Dashboard metrics:

CPU

Memory

Disk

Network

Load

Uptime

📚 What I Learned
AWS EC2

Linux Administration

Docker

Git & GitHub

GitHub Actions

CI/CD

SSH Deployment

Nginx

Prometheus

Node Exporter

Grafana

Cloud Resource Management

🎯 Future Improvements
HTTPS with SSL/TLS

Custom Domain

AWS ECR Integration

Docker Compose

Deployment Health Checks

Automated Rollback

Terraform Infrastructure

Kubernetes Deployment

📌 Project Status
Completed ✅

The Flask application, Docker deployment, CI/CD pipeline, Nginx configuration, and monitoring stack were successfully implemented and tested.

AWS resources were decommissioned after project completion to avoid unnecessary ongoing cloud costs.

👩‍💻 Author
Shital Dhaval

GitHub:

https://github.com/shitaldhaval2004/employee-devops-project

⭐ Project Highlights
Cloud: AWS EC2
Containerization: Docker
CI/CD: GitHub Actions
Web Server: Nginx
Application: Python Flask
Monitoring: Prometheus + Node Exporter + Grafana
