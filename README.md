# Kubernetes CI/CD Pipeline using Jenkins, Docker & Minikube

## Project Overview

This project demonstrates a complete CI/CD pipeline using GitHub, Jenkins, Docker, Kubernetes, and Minikube.

The application is automatically built, containerized, and deployed to a Kubernetes cluster whenever changes are pushed to the GitHub repository.

This project simulates a real-world DevOps workflow where application updates are continuously delivered through an automated deployment pipeline.

---

## Architecture

```text
Developer
    ↓
GitHub Repository
    ↓
Jenkins Pipeline
    ↓
Docker Image Build
    ↓
Minikube Image Load
    ↓
Kubernetes Deployment
    ↓
Rolling Update
    ↓
Application Available to Users
```

---

## Technologies Used

- Git
- GitHub
- Jenkins
- Docker
- Kubernetes
- Minikube
- HTML
- YAML

---

## Project Structure

```text
kubernetes-cicd-project/
│
├── index.html
├── Dockerfile
├── deployment.yaml
├── service.yaml
├── Jenkinsfile
└── README.md
```

---

## Features

- Automated CI/CD Pipeline
- Docker Image Creation
- Kubernetes Deployment
- NodePort Service Exposure
- Rolling Updates
- Multi-Pod Deployment
- Automated Deployment Verification
- Infrastructure Automation

---

## Kubernetes Components

### Deployment

Manages application pods and ensures desired replicas are running.

```yaml
Replicas: 2
```

### Service

Exposes the application through a Kubernetes NodePort service.

```yaml
Type: NodePort
```

### Pods

Application instances running inside the Kubernetes cluster.

---

## Jenkins Pipeline Stages

### 1. Checkout Source Code

Pulls the latest code from GitHub.

### 2. Build Docker Image

Creates a new Docker image using the Dockerfile.

### 3. Load Image into Minikube

Transfers the Docker image into the Minikube cluster.

### 4. Deploy to Kubernetes

Applies Deployment and Service manifests.

### 5. Rolling Update

Restarts the deployment and updates running pods without downtime.

### 6. Verify Deployment

Checks pod status after deployment.

---

## Pipeline Workflow

```text
GitHub Push
      ↓
Jenkins Trigger
      ↓
Build Docker Image
      ↓
Load Image to Minikube
      ↓
Deploy to Kubernetes
      ↓
Rolling Update
      ↓
Verify Deployment
      ↓
Application Available
```

---

## Commands Used

### Deploy Application

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### View Pods

```bash
kubectl get pods
```

### View Deployments

```bash
kubectl get deployments
```

### View Services

```bash
kubectl get svc
```

### Restart Deployment

```bash
kubectl rollout restart deployment cicd-app
```

---

## Jenkins Pipeline 

<img width="1920" height="1080" alt="Screenshot (1018)" src="https://github.com/user-attachments/assets/fd6035a2-9fba-4354-a24f-412cb560cca7" />


---

## Jenkins Console Output
<img width="1920" height="1080" alt="Screenshot (1019)" src="https://github.com/user-attachments/assets/5c9a605f-3d0d-480c-99c3-1e5e695cf9b4" />


---

## Kubernetes Application Running

<img width="1920" height="1080" alt="Screenshot (1013)" src="https://github.com/user-attachments/assets/8c4d35b5-ca31-4723-934d-1814cc8f4bb2" />


---



---

## Learning Outcomes

Through this project I learned:

- CI/CD Pipeline Implementation
- Jenkins Pipeline Automation
- Docker Containerization
- Kubernetes Deployments
- Kubernetes Services
- Rolling Updates
- Pod Management
- Application Deployment Automation
- DevOps Best Practices

---

## Real-World Use Case

This project represents a simplified version of how modern organizations automate application deployment using Kubernetes and Jenkins.

The same workflow can be extended to production environments using:

- AWS EKS
- Azure AKS
- Google GKE
- ArgoCD
- Helm
- Docker Hub
- Amazon ECR

---

## Author

**Amruthesh S P**

