# 🚀 3-Tier DevSecOps Project

This is a production-grade **3-tier web application** deployed using **DevSecOps best practices**, integrating CI/CD pipelines, Infrastructure as Code, container orchestration, and automated security checks. The project is built to run across **Dev, QA, and Prod** environments with real-time monitoring and alerting.

---

## 🛠️ Tech Stack & Tools

<p align="left">
  <img src="https://img.shields.io/badge/Jenkins-%232C5263.svg?logo=jenkins&logoColor=white" />
  <img src="https://img.shields.io/badge/Kubernetes-%23326CE5.svg?logo=kubernetes&logoColor=white" />
  <img src="https://img.shields.io/badge/Terraform-%235835CC.svg?logo=terraform&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS-EKS-orange?logo=amazonaws&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-%230db7ed.svg?logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/SonarQube-%2300B0FF.svg?logo=sonarqube&logoColor=white" />
  <img src="https://img.shields.io/badge/Trivy-%23C12127.svg?logo=trivy&logoColor=white" />
  <img src="https://img.shields.io/badge/Gitleaks-%23323A3F.svg?logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/Grafana-%23F46800.svg?logo=grafana&logoColor=white" />
  <img src="https://img.shields.io/badge/Slack-%234A154B.svg?logo=slack&logoColor=white" />
</p>

---

---

## 🧩 Project Architecture

      GitHub Repository
              ↓
          Jenkins CI
              ↓
 ┌────────────────────────┐
 │  Security Scanning     │
 │  (Gitleaks, Trivy,     │
 │   SonarQube)           │
 └────────────────────────┘
              ↓
     Terraform Provisioning
              ↓
        AWS EKS Cluster
              ↓
     3-Tier App Deployment
              ↓
    Grafana + Slack Alerts



---

## 🔐 Security Integration

This project incorporates essential security scanning tools as part of the CI/CD lifecycle:

- **Gitleaks**: Scans codebase for hardcoded secrets and credentials.
- **Trivy**: Scans Docker images for OS and application vulnerabilities.
- **SonarQube**: Performs static code analysis to detect code smells, bugs, and security hotspots.

---

## 🔁 CI/CD Pipeline Flow

The Jenkins pipeline (saved as `Jenkins-pipeline`) automates:

1. Clone and scan source code from GitHub.
2. Run static analysis (SonarQube) and secret detection (Gitleaks).
3. Build Docker image and push to Docker Hub.
4. Provision infrastructure using Terraform.
5. Deploy the 3-tier app to an EKS cluster.
6. Monitor the system using Grafana dashboards.
7. Send alerts to Slack for failures and warnings.

---

## 🧪 How to Run This Project

### 🔧 Prerequisites

- AWS CLI configured with valid credentials
- Terraform installed and in system path
- Jenkins master with Docker agents set up
- IAM roles for EKS provisioning via Terraform
- GitHub repository configured with webhook (to trigger Jenkins job)

---

### 📦 Steps to Deploy

#### 1. Clone the Repository

git clone https://github.com/namrqthakaipa/3-tier-devsecops-project.git
cd 3-tier-devsecops-project

