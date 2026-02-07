# 🚀 Kubernetes Helm DevOps Project

Production-oriented DevOps project demonstrating deployment, configuration, scaling, and testing of a containerized Flask application using Kubernetes and Helm.

The project focuses on real-world Kubernetes workload patterns and operational concerns rather than application complexity.

## 📋 Project Overview

This repository showcases a complete DevOps workflow built around a minimal Flask service, designed to highlight:

* Kubernetes resource management

* Helm-based application packaging

* Configuration and secrets handling

* Autoscaling and background jobs

* Application health checks and testing

The application itself is intentionally simple to keep the emphasis on infrastructure behavior and orchestration.

## 🏗 Architecture & Flow

The deployment flow follows standard cloud-native practices:

1. Flask application is containerized using Docker

2. Application is packaged and deployed using a Helm chart

3. Kubernetes resources are created and managed declaratively

4. Configuration and secrets are injected at runtime

5. Application is exposed via Service and Ingress

6. Scaling and background tasks are handled by native Kubernetes primitives

Flask App
   ➜ Docker Image
   ➜ Helm Chart
   ➜ Kubernetes Cluster
       ├── Deployment
       ├── Service
       ├── Ingress
       ├── ConfigMap
       ├── Secret
       ├── HPA
       ├── CronJob
       └── PersistentVolumeClaim

## 🛠 Tech Stack
Category	Technologies
Language	Python
Framework	Flask
Containerization	Docker
Orchestration	Kubernetes
Packaging	Helm
Configuration	ConfigMap, Secrets
Scaling	Horizontal Pod Autoscaler (HPA)
Scheduling	Kubernetes CronJob
Networking	Service, Ingress
Storage	PersistentVolumeClaim
Testing	Python unit tests
Automation	Declarative YAML
## 📦 Application Details
**Endpoints**

* / – basic response with injected secret

* /health – health check endpoint for Kubernetes readiness/liveness usage

Environment variables and secrets are injected at runtime using Kubernetes resources.

## 🧪 Testing

The project includes application-level unit tests to validate:

* Application startup

* Root endpoint response

* Health endpoint availability

Run tests locally:

 python -m unittest -v


Testing is designed to be CI-friendly and easily integrated into automated pipelines.

## 📁 Repository Structure
kubernetes-helm-devops-project/
├── app.py                 # Flask application
├── test_app.py            # Application unit tests
├── requirements.txt       # Python dependencies
├── Dockerfile             # Container definition
├── docker-compose.yaml    # Local development support
│
├── Chart.yaml             # Helm chart metadata
├── values.yaml            # Helm configuration values
├── templates/
│   ├── deployment.yaml    # Application deployment
│   ├── service.yaml       # Cluster service
│   ├── ingress.yaml       # Ingress configuration
│   ├── configmap.yaml     # Application configuration
│   ├── secret.yaml        # Secrets injection
│   ├── hpa.yaml           # Horizontal Pod Autoscaler
│   ├── cronjob.yaml       # Scheduled background job
│   ├── pvc.yaml           # Persistent storage
│   └── test-connection.yaml
│
├── .helmignore
├── .gitignore
└── README.md

## 🚀 Deployment (Helm)

Install the application using Helm:

helm install my-app .


Upgrade an existing release:

helm upgrade my-app .


Uninstall:

helm uninstall my-app

## 🎯 What This Project Demonstrates

* Kubernetes-native application design

* Helm-based deployment and configuration management
 
* Secure handling of configuration and secrets

* Autoscaling using HPA

* Scheduled background processing with CronJobs

* Health checks and application testing

* Clean separation between application code and infrastructure

## 🚧 Limitations & Future Improvements

This project focuses on Kubernetes and Helm fundamentals. Planned enhancements include:

* CI/CD pipeline integration (GitHub Actions)

* Terraform-based infrastructure provisioning

* Centralized logging and monitoring (Prometheus & Grafana)

* External cloud load balancer integration

* Advanced rollout strategies (blue/green, canary)

## 👤 Author

DevOps Engineer (Junior / Entry Level)
Focused on Kubernetes, Automation, and Cloud-Native Infrastructure

## ⚖️ License

Personal DevOps portfolio project.
