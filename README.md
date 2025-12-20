<div align="center">
  <img src="./public/assets/DevSecOps.png" alt="Logo" width="100%" height="100%">

  <br>
  <a href="http://netflix-clone-with-tmdb-using-react-mui.vercel.app/">
    <img src="./public/assets/netflix-logo.png" alt="Logo" width="100" height="32">
  </a>
</div>

<br />

<div align="center">
  <img src="./public/assets/home-page.png" alt="Logo" width="100%" height="100%">
  <p align="center">Home Page</p>
</div>


# 🎬 DevSecOps Netflix Clone Project

An end-to-end **DevSecOps project** implementing CI/CD automation, security scanning, monitoring, Kubernetes deployment, and GitOps on AWS.

---

## 🚀 Project Overview

This project demonstrates how to build and deploy a Netflix-like application using modern **DevSecOps practices**.  
It integrates CI/CD, security, monitoring, Kubernetes (EKS), and GitOps using industry-standard tools.

---

## 🛠️ Tech Stack

**CI/CD & Security**
- Jenkins
- SonarQube
- OWASP Dependency-Check
- Trivy
- Docker

**Monitoring**
- Prometheus
- Node Exporter
- Grafana

**Container Orchestration & GitOps**
- Amazon EKS
- ArgoCD

**Cloud**
- AWS EC2
- AWS EKS
- AWS CloudFormation (via eksctl)

---

## 🧩 Architecture

- Jenkins automates build, test, security scan, and deployment
- SonarQube enforces code quality and security gates
- Trivy scans filesystem and container images for vulnerabilities
- Docker packages the application
- Application is deployed to Amazon EKS
- ArgoCD manages GitOps-based deployment
- Prometheus and Grafana provide monitoring and observability

---

## 🔁 CI/CD Pipeline Flow

1. Code checkout from GitHub
2. SonarQube static code analysis
3. Quality Gate validation
4. Dependency vulnerability scan (OWASP)
5. Trivy filesystem scan
6. Docker image build
7. Trivy image scan
8. Application deployment

---



---
## Kubernetes & GitOps

- EKS cluster created using `eksctl`
- Application deployed on Kubernetes
- ArgoCD used for GitOps-based continuous deployment
- Application exposed via NodePort

---

## Monitoring

- Prometheus collects metrics from nodes and services
- Grafana visualizes CPU, memory, disk, and network metrics

---
## ☸️ Kubernetes Setup

EKS cluster created using eksctl:

```bash
eksctl create cluster \
--name Netflix \
--region ap-south-1 \
--version 1.31 \
--nodegroup-name n \
--node-type t3.medium \
--nodes 1 \
--nodes-min 1 \
--nodes-max 1 \
--managed
```

## Cleanup

```bash
eksctl delete cluster --name Netflix --region ap-south-1
```

📸 Screenshots

Screenshots are available in the screenshots/ directory and include:

      Jenkins Pipeline  
      SonarQube Quality Gate
      Netflix Application UI
      Prometheus Targets
      Grafana Dashboards
      Kubernetes Pods
      ArgoCD Application Sync
      AWS Infrastructure


✅ Key Learnings

Built a complete DevSecOps CI/CD pipeline
Implemented shift-left security
Deployed containerized application on AWS EKS
Practiced GitOps using ArgoCD
Implemented monitoring and observability



👨‍💻 Author

Harish Reddy
DevOps / DevSecOps Engineer
