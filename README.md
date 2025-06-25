# 📚 Book-Reviews

## 📌 Project Overview  
This project demonstrates a complete DevOps pipeline for deploying a microservices-based application on a self-hosted Kubernetes cluster (provisioned with `kubeadm` on AWS EC2).  
It covers infrastructure provisioning, CI/CD, container security, GitOps deployment, and monitoring.

---

## ⚙️ Technologies Used

- **IaC**: Terraform, Bash  
- **Cloud Platform**: AWS EC2  
- **Containerization & Orchestration**: Docker, Kubernetes (kubeadm), Helm  
- **CI/CD**: Jenkins, GitHub, Argo CD  
- **Security**: Trivy, Harbor  
- **Monitoring**: Prometheus, Grafana, Slack  
- **Microservices**: Spring Boot, Kafka, MongoDB

---

## 🚀 Architecture Overview

- Terraform provisions VPC, EC2 instances, security groups  
- Bash scripts bootstrap a multi-node Kubernetes cluster using `kubeadm`  
- Jenkins builds source code (Maven), runs SonarQube checks, builds Docker images  
- Trivy scans Docker images for vulnerabilities before pushing to Harbor  
- Kubernetes manifests & Helm charts define deployment for each service  
- Argo CD syncs manifests from GitHub to K8s (GitOps)  
- Prometheus & Grafana monitor cluster and app metrics; alerts sent via Slack  
- Spring Boot microservices communicate via Kafka and store data in MongoDB  

---

## 🧭 Architecture Diagram

![Architecture](images/AWS_Architecture.png)
