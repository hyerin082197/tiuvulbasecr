# CI/CD Workflow with Vulnerability Scanning

This repository demonstrates a **CI/CD pipeline** using **GitHub Actions**, which includes Docker image building, vulnerability scanning with **Trivy**, and Slack notifications for success or failure.

## Features
1. Automatically build and push Docker images to **Azure Container Registry (ACR)**
2. Perform vulnerability scanning on Docker images using **Trivy**
3. Notify results (success or failure) via **Slack**
4. Supports critical and high-severity vulnerability detection

## Technology Stack
- **GitHub Actions**: Workflow automation
- **Docker**: Containerization and image management
- **Trivy**: Vulnerability scanner for Docker images
- **Slack**: Notifications for workflow results

## Workflow Overview
1. **Trigger**: The workflow runs on push or pull request to the `main` branch
2. **Steps**
   - Checkout repository code
   - Install required tools (Docker, Trivy)
   - Build Docker image
   - Push Docker image to ACR
   - Scan Docker image for vulnerabilities
   - Send Slack notifications based on scan results


## File Structure
.
├── .github/
│   └── workflows/
│       └── cicd.yml    # The GitHub Actions workflow
├── Dockerfile          # Docker image configuration
├── README.md           # Project documentation
└── .gitignore          # Ignored files
