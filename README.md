DevOps Documents & Hands-On Guides


A practical collection of DevOps setup guides, configuration notes, commands, and hands-on project documentation covering containerization, CI/CD, Kubernetes, AWS, automation, code quality, artifact management, monitoring, logging, and databases.

This repository is intended as a learning reference and practical DevOps handbook for building and troubleshooting common DevOps environments.

📚 Documentation

The repository currently contains the following guides:

#

Document

Topic

01

Jenkins Server Setup

Jenkins Server Setup

02

Docker Setup

Docker Setup

03

Docker Compose Setup

Docker Compose Setup

04

Jenkins Docker Project

Jenkins Docker Project

05

Eks Setup

Eks Setup

06

Sonar Setup Docker

Sonar Setup Docker

07

Nexus Setup Docker

Nexus Setup Docker

08

Elk Stack Setup

Elk Stack Setup

09

Devops Project Setup

Devops Project Setup

10

Jenkins Docker K8S

Jenkins Docker K8S

11

Ansible Setup

Ansible Setup

12

Mysql Db Setup

Mysql Db Setup

13

Minikube Setup

Minikube Setup

🛠️ Technologies Covered

This repository brings together documentation for a broad DevOps toolchain:

AWS — EC2, EKS and cloud infrastructure

Jenkins — CI/CD automation

Docker — Containers, images and Docker-based deployments

Docker Compose — Multi-container applications

Kubernetes — Container orchestration

Amazon EKS — Managed Kubernetes on AWS

Minikube — Local Kubernetes development

Ansible — Configuration management and automation

SonarQube — Static code analysis and code quality

Nexus Repository — Artifact and package management

ELK Stack — Elasticsearch, Logstash and Kibana

MySQL — Relational database setup and configuration

🎯 Learning Objectives

By working through these documents, you can build practical knowledge of:

Setting up DevOps tools on Linux/AWS environments.

Creating and managing Docker images and containers.

Running multi-container applications with Docker Compose.

Building CI/CD pipelines with Jenkins.

Integrating Jenkins with Docker and Kubernetes.

Deploying workloads to Kubernetes and Amazon EKS.

Managing infrastructure and configuration with Ansible.

Performing code-quality analysis with SonarQube.

Managing build artifacts with Nexus Repository.

Collecting and visualizing application logs with the ELK Stack.

Running Kubernetes locally with Minikube.

Configuring MySQL for application and DevOps environments.

🏗️ Suggested Learning Path

If you are using this repository as a structured learning path, the following order is recommended:

Linux / AWS Basics
       │
       ▼
Jenkins ───────► CI/CD Fundamentals
       │
       ▼
Docker ────────► Containerization
       │
       ▼
Docker Compose ► Multi-container Applications
       │
       ▼
SonarQube ─────► Code Quality
       │
       ▼
Nexus ─────────► Artifact Management
       │
       ▼
Kubernetes ────► Container Orchestration
       │
       ├──────► Minikube
       │
       └──────► Amazon EKS
       │
       ▼
Jenkins + Docker + Kubernetes
       │
       ▼
Ansible + ELK + MySQL
       │
       ▼
End-to-End DevOps Project

🚀 Getting Started

Prerequisites

The exact requirements depend on the guide you are following, but a typical environment may include:

Linux / Amazon Linux

AWS account for cloud-based exercises

Git

Docker

Docker Compose

Java

Maven

Jenkins

Kubernetes / kubectl

Minikube

Ansible

MySQL

Note: Do not install every tool at once. Follow the individual documentation and install only the components required for the exercise you are working on.

💻 Working With the Repository

Clone the repository:

git clone https://github.com/Chaitanya4K/java-devops-handbook.git

Move into the repository:

cd DevOps-Documents

Open any guide with your preferred Markdown editor or GitHub's built-in Markdown viewer.

🔐 Security Best Practices

When using these guides with AWS, Docker, Jenkins, Kubernetes, or other infrastructure tools:

Never commit AWS access keys, secret keys, passwords, private keys, or tokens.

Do not upload .pem files or SSH private keys to GitHub.

Use environment variables or a secrets-management solution for sensitive values.

Review configuration files before committing them.

Avoid hard-coding database passwords and API credentials.

Restrict AWS security-group rules to the minimum required access.

Remove unused cloud resources to avoid unexpected charges.

Use .gitignore for local credentials, generated files, logs, and environment files.

Example .gitignore entries:

# Environment / secrets
.env
*.pem
*.key

# Logs
*.log
logs/

# IDE
.idea/
.vscode/

# Build output
target/

🧪 Hands-On Approach

The goal of this repository is not just to collect commands. Each guide can be used as a hands-on exercise:

Read
  ↓
Configure
  ↓
Run
  ↓
Verify
  ↓
Troubleshoot
  ↓
Document
  ↓
Repeat

When practicing, make sure you understand why each command is being used instead of only copying commands.

📌 Repository Structure

DevOps-Documents/
│
├── README.md
├── 01-Jenkins-Server-Setup.md
├── 02-Docker-Setup.md
├── 03-Docker-Compose-Setup.md
├── ...
├── 12_MySQL_DB_Setup.md
└── 13_MiniKube_Setup.md

🤝 Contributing

Suggestions, corrections, improvements, and additional DevOps examples are welcome.

A simple contribution workflow:

git checkout -b feature/improve-documentation
git add .
git commit -m "Improve DevOps documentation"
git push origin feature/improve-documentation

Then open a Pull Request on GitHub.

⭐ Purpose of This Repository

This repository is maintained as a practical DevOps learning and reference resource. It brings together setup instructions and hands-on notes so that common DevOps tools can be installed, configured, tested, and integrated into real-world workflows.

If you find the documentation useful, consider giving the repository a ⭐ on GitHub.

👤 Author

Chaitanya K

DevOps / Java / Cloud learning projects and hands-on documentation.

📄 License

Unless otherwise specified, the documentation in this repository is provided for learning and educational purposes.

Keep learning. Keep building. Keep automating. 🚀
