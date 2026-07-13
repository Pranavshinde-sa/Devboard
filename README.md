# DevBoard – DevOps Implementation

## Overview

This repository demonstrates the end-to-end DevOps implementation of the **DevBoard** application.

> **Note**
>
> The original application source code (frontend and backend business logic) was **not developed by me**. It is based on the DevBoard application created by the original author.
>
> My contribution is focused entirely on the **DevOps, containerization, deployment, infrastructure, and automation implementation**. All Docker, CI/CD, deployment, infrastructure, and automation work in this repository is my own.

---

## DevOps Objectives

The goal of this project is to take an existing full-stack application and deploy it using production-oriented DevOps practices.

Current progress includes:

* Multi-stage Docker builds
* Docker image optimization
* Non-root container execution
* Docker networking
* PostgreSQL container deployment
* Frontend, backend, and database containerization
* Three-tier application deployment on AWS EC2
* Docker Compose for multi-container application management
* GitHub Actions Continuous Integration (CI)
* GitHub Actions Continuous Deployment (CD)

Future improvements include:

* Kubernetes deployment
* Infrastructure as Code
* Monitoring and observability

---

## Architecture

```text
Browser
    │
    ▼
Frontend Container
    │
    ▼
Backend Container
    │
    ▼
PostgreSQL Container
```

All containers communicate through a dedicated Docker network.

---

## Technologies

### Application

* React
* Vite
* Go
* PostgreSQL

### DevOps

* Docker
* Docker Compose
* Docker Networking
* Multi-stage Dockerfiles
* GitHub Actions
* AWS EC2
* Linux
* Git
* GitHub
* Docker
* Docker Compose
* Docker Networking

---

# Progress

## ✅ Phase 1 — Containerization

* Containerized frontend
* Containerized backend
* Multi-stage Docker builds
* Reduced image size
* Added `.dockerignore`
* Configured non-root users
* Exposed required ports

---

## ✅ Phase 2 — Docker Networking

* Created dedicated Docker network
* Connected frontend, backend, and PostgreSQL
* Configured container-to-container communication
* Verified backend database connectivity

---

## ✅ Phase 3 — Database Deployment

* PostgreSQL container deployment
* Database initialization scripts
* Persistent database configuration
* Application successfully connected to PostgreSQL

---

## ✅ Phase 4 — AWS EC2 Deployment

* Provisioned EC2 instance
* Installed Docker
* Built and deployed application containers
* Started frontend, backend, and PostgreSQL services
* Successfully deployed the complete three-tier application

---

## ✅ Phase 5 — Docker Compose

- Created Docker Compose configuration
- Defined frontend, backend, and PostgreSQL services
- Managed application networking with Docker Compose
- Configured environment variables and persistent volumes
- Started the complete application with a single command

---

## ✅ Phase 6 — CI/CD Automation

### Continuous Integration (CI)

* Configured GitHub Actions CI workflow
* Automated frontend build and validation
* Built Docker images for frontend and backend
* Pushed versioned images to Docker Hub

### Continuous Deployment (CD)

* Configured GitHub Actions CD workflow
* Used a self-hosted GitHub Actions runner on AWS EC2
* Automatically pulled the latest Docker images
* Deployed updated containers using Docker Compose
* Automated application deployment after successful CI

---

# Repository Structure

```text
.
├── .github/
│   └── workflows/
|       ├── ci-cd.yml
│       ├── ci.yml
│       └── cd.yml
│
├── frontend/
│   ├── Dockerfile
│   └── .dockerignore
│
├── backend/
│   ├── Dockerfile
│   └── .dockerignore
│
├── init/
│   └── postgres/
│
├── docker-compose.yml
├── docker-compose.prod.yml
└── README.md
```

---

# Learning Goals

This repository demonstrates practical DevOps skills including:

* Docker image creation
* Multi-stage Docker builds
* Container security
* Docker networking
* GitHub Actions CI/CD
* Linux server administration
* AWS EC2 deployment
* Production deployment workflow
* Automated application delivery

---

# Roadmap

* [x] Dockerize frontend
* [x] Dockerize backend
* [x] Dockerize PostgreSQL
* [x] Configure Docker networking
* [x] Deploy three-tier application to AWS EC2
* [x] Configure Docker Compose production
* [x] Implement GitHub Actions CI
* [x] Implement GitHub Actions CD
* [x] Kubernetes deployment
* [ ] Infrastructure as Code (Terraform)
* [ ] Monitoring & Logging

---

## Attribution

The DevBoard application itself was originally developed by its respective author.

This repository is maintained as a **DevOps implementation project** demonstrating containerization, CI/CD automation, deployment, infrastructure, and production-oriented DevOps practices built on top of the original application.
