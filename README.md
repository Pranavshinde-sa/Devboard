# DevBoard – DevOps Implementation

## Overview

This repository demonstrates the end-to-end DevOps implementation of the **DevBoard** application.

> **Note**
>
> The original application source code (frontend and backend business logic) was **not developed by me**. It is based on the DevBoard application created by the original author.
>
> My contribution is focused entirely on the **DevOps, containerization, deployment, and infrastructure implementation**. All Docker, deployment, infrastructure, and automation work in this repository is my own.

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

Future improvements include:

* Nginx reverse proxy
* GitHub Actions CI
* GitHub Actions CD
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
* Docker Networking
* Multi-stage Dockerfiles
* AWS EC2
* Linux
* Git
* GitHub

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

* PostgreSQL container
* Database initialization scripts
* Persistent database configuration
* Application successfully connected to PostgreSQL

---

## ✅ Phase 4 — AWS EC2 Deployment

* Provisioned EC2 instance
* Installed Docker
* Built Docker images on EC2
* Started frontend, backend, and PostgreSQL containers
* Deployed complete three-tier application

---

# Repository Structure

```text
.
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
└── README.md
```

---

# Learning Goals

This repository is intended to demonstrate practical DevOps skills including:

* Docker image creation
* Multi-stage builds
* Container security
* Docker networking
* Linux deployment
* AWS EC2 deployment
* Production deployment workflow

---

# Roadmap

* [x] Dockerize frontend
* [x] Dockerize backend
* [x] Dockerize PostgreSQL
* [x] Configure Docker networking
* [x] Deploy three-tier application to AWS EC2
* [ ] Configure Nginx reverse proxy
* [ ] Add GitHub Actions CI
* [ ] Add GitHub Actions CD
* [ ] Infrastructure as Code
* [ ] Monitoring & Logging

---

## Attribution

The DevBoard application itself was originally developed by its respective author.

This repository is maintained as a **DevOps implementation project** demonstrating deployment, containerization, infrastructure, and automation practices on top of the existing application.
