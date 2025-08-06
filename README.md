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

## 🧩 Project Architecture

```bash
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
