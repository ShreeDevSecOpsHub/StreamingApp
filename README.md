
# StreamingApp - MERN Stack with Docker, Jenkins CI/CD & Kubernetes (EKS)

A complete **DevOps project** demonstrating containerization, CI/CD pipeline, orchestration, scaling, and monitoring of a MERN-based Streaming Application.

---

## 📋 Project Overview

This project involves containerizing a multi-service MERN Streaming Application, setting up a complete CI/CD pipeline using **Jenkins**, deploying it on **Amazon EKS** using **Helm**, and implementing monitoring & logging with AWS services.

---

## 🛠 Tech Stack

- **Frontend**: React.js
- **Backend**: Node.js + Express (Microservices)
- **Database**: MongoDB
- **Containerization**: Docker
- **CI/CD**: Jenkins
- **Container Registry**: Amazon ECR
- **Orchestration**: Kubernetes (Amazon EKS)
- **Package Manager**: Helm
- **Monitoring**: Amazon CloudWatch + Container Insights
- **Infrastructure**: AWS

---

## 📁 Project Structure

```
StreamingApp/
├── backend/
│   ├── authService/
│   ├── streamingService/
│   ├── adminService/
│   └── chatService/
├── frontend/
├── k8s/                    # Kubernetes manifests (optional)
├── helm-chart/             # Helm charts
├── Jenkinsfile
├── docker-compose.yml
├── Dockerfile (per service)
└── docs/
```

---

## 🚀 Setup and Deployment Steps

### 1. Version Control & Fork
- Forked from: [https://github.com/UnpredictablePrashant/StreamingApp.git](https://github.com/UnpredictablePrashant/StreamingApp.git)
- Synced with upstream regularly.

### 2. Containerization

**Dockerfiles** created for:
- Frontend (Multi-stage build with Nginx)
- Each Backend Service (auth, streaming, admin, chat)

**Pushed images to Amazon ECR**

### 3. Continuous Integration (CI)

- Jenkins installed on AWS EC2
- Jenkins Pipeline (`Jenkinsfile`) automatically:
  - Builds Docker images
  - Pushes to Amazon ECR
  - Triggered on every push to GitHub

### 4. Kubernetes Deployment (Amazon EKS)

- EKS Cluster created using `eksctl`
- Deployed using **Helm charts**
- Horizontal Pod Autoscaler (HPA) configured for scaling
- AWS Load Balancer Controller for Ingress

### 5. Monitoring & Logging

- Amazon CloudWatch Container Insights
- CloudWatch Logs for centralized logging
- Alarms configured for critical metrics

### 6. Bonus: ChatOps Integration

- SNS Topics created for deployment notifications
- Integrated with Slack / Teams / Telegram for real-time alerts

---

## 📊 Architecture Diagram

*(Add your architecture diagram here - PNG/SVG)*

![System Architecture](./docs/architecture-diagram.png)

---

## 🧪 How to Run Locally

```bash
docker-compose up --build
```

---

## 📝 Documentation

- [Deployment Guide](./docs/DEPLOYMENT.md)
- [Jenkins Pipeline](./Jenkinsfile)
- [Helm Charts](./helm-chart/)
- [Infrastructure Setup](./docs/AWS_SETUP.md)

---

## ✅ Final Validation

- Frontend and Backend services are accessible via Load Balancer
- Auto-scaling is working
- CI/CD pipeline is fully functional
- Logging and monitoring are active

---

## 📬 Contact

**Name**: Shreeram Parab  
**Location**: Pune, Maharashtra

---

## 🔗 Repository Link

[https://github.com/YOUR-USERNAME/StreamingApp](https://github.com/YOUR-USERNAME/StreamingApp)

---

**Project completed as part of HeroVired Graded Assignment on Orchestration and Scaling.**

---

```

### How to Use This:

1. Go to your GitHub repository
2. Click on **Add a README** or edit existing `README.md`
3. Paste the entire content above
4. Replace `YOUR-USERNAME` with your actual GitHub username
5. Add your architecture diagram in the `docs/` folder and update the path
6. Commit the file

Would you like me to also create separate files like:
- `docs/DEPLOYMENT.md`
- `docs/AWS_SETUP.md`
- A detailed Helm values example

Just say the word and I’ll generate them for you.
