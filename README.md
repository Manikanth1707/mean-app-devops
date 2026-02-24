# 🚀 Production-Ready MEAN Stack Application with Docker & CI/CD

## 📖 Project Description

This project demonstrates the deployment of a full-stack MEAN (MongoDB, Express.js, Angular, Node.js) application using Docker containerization and a fully automated CI/CD pipeline.

The application is deployed on AWS EC2 and integrates Docker Hub and GitHub Actions to enable automated build and deployment workflows on every push to the main branch.

---

## 📌 Application Overview

The application is a CRUD-based tutorial management system that allows users to:

- Create tutorials
- Retrieve tutorials
- Update tutorials
- Delete tutorials
- Persist data using MongoDB

The entire stack is containerized to ensure consistency across development and production environments.

---

## 🏗️ System Architecture

### Application Flow

Client (Browser)  
→ Nginx (Angular Frontend Container)  
→ Node.js + Express REST API (Backend Container)  
→ MongoDB (Database Container)

### Deployment Workflow

Developer Push  
→ GitHub Repository  
→ GitHub Actions CI/CD Pipeline  
→ Docker Image Build  
→ Push to Docker Hub  
→ Automated Deployment to AWS EC2  
→ Containers Restart with Updated Images  

---

## 🐳 Containerization Strategy

The application is divided into three Docker containers:

1. **Frontend Container**
   - Angular application
   - Served using Nginx

2. **Backend Container**
   - Node.js + Express REST API
   - Handles business logic and database communication

3. **Database Container**
   - Official MongoDB image (`mongo:6`)

Docker Hub Repositories:

- `manikanth1709/mean-frontend`
- `manikanth1709/mean-backend`

---

## ☁️ Cloud Deployment (AWS EC2)

- Instance Type: t3.micro
- Operating System: Ubuntu 22.04 LTS
- Container Orchestration: Docker Compose
- Security Group Configuration:
  - Port 22 (SSH)
  - Port 80 (Frontend)
  - Port 8080 (Backend API)

The application is publicly accessible via the EC2 public IP address.

http://<EC2-Public-IP>
---

## 🔁 Continuous Integration & Continuous Deployment (CI/CD)

A GitHub Actions workflow is configured to automatically:

1. Build backend Docker image
2. Build frontend Docker image
3. Push images to Docker Hub
4. Connect to EC2 via SSH
5. Pull latest images
6. Restart services using Docker Compose

This enables zero manual deployment and ensures continuous delivery.

---

## 🔐 Security Considerations

- SSH key-based authentication for EC2 access
- Restricted inbound ports via AWS Security Groups
- Container isolation using Docker networking
- No hardcoded credentials inside source code

---

## 🧪 Validation & Verification

The deployment was verified using:

- Docker container status (`docker ps`)
- GitHub Actions workflow success logs
- Docker Hub repository confirmation
- EC2 instance health checks
- Functional testing via public IP access

---

## 🧰 Technologies Used

- Angular 15
- Node.js
- Express.js
- MongoDB
- Docker
- Docker Compose
- GitHub Actions
- AWS EC2
- Nginx

---

## ✅ Project Outcome

This project successfully demonstrates:

- End-to-end containerization of a full-stack application
- Automated CI/CD pipeline implementation
- Cloud deployment on AWS
- Production-style DevOps workflow integration

---

## 👨‍💻 Author

Manikanth  
DevOps & Cloud Deployment Project