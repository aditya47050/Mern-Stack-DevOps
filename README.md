# MERN Todo App with DevOps Deployment

A full-stack **MERN Todo Application** containerized with **Docker**, automated using **CI/CD**, and deployed on **AWS EC2**.

This project demonstrates a complete **DevOps workflow** from development to production deployment.

---

# Project Overview

This project implements a Todo application using the **MERN stack**:

* MongoDB Atlas (Database)
* Express.js (Backend API)
* React.js (Frontend)
* Node.js (Runtime)

The application is containerized with Docker, integrated with a CI pipeline, and deployed to a cloud server.

---

# Tech Stack

Frontend

* React.js
* Axios

Backend

* Node.js
* Express.js

Database

* MongoDB Atlas

DevOps & Infrastructure

* Docker
* Docker Hub
* GitHub Actions
* AWS EC2

---

# Architecture

User
│
Internet
│
AWS EC2
│
Docker Containers
│      │
Frontend Backend
│
MongoDB Atlas

---

# DevOps Workflow

The project follows a complete DevOps pipeline:

Code Push
↓
GitHub Repository
↓
GitHub Actions CI Pipeline
↓
Docker Image Build
↓
Push to Docker Hub
↓
AWS EC2 Deployment
↓
Docker Containers Running Application

---

# Features

* Create Todo Task
* View Existing Tasks
* Update Tasks
* Delete Tasks
* Persistent data using MongoDB Atlas
* Containerized deployment
* CI pipeline for Docker builds
* Cloud deployment using AWS EC2

---

# Project Structure

```
MERN-Stack-DevOps
│
├── TODO
│   ├── todo_backend
│   │   ├── models
│   │   ├── server.js
│   │   └── package.json
│   │
│   └── todo_frontend
│       ├── src
│       └── package.json
│
├── docker-compose.yml
├── .github/workflows/ci.yml
├── Dockerfile
└── README.md
```

---

# Environment Variables

Backend requires the following environment variables:

```
PORT=3001
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/TODO
```

---

# Running Locally

Clone repository:

```
git clone https://github.com/<your-username>/Mern-Stack-DevOps.git
```

Install dependencies:

Backend:

```
cd TODO/todo_backend
npm install
```

Frontend:

```
cd TODO/todo_frontend
npm install
```

Run backend:

```
npm start
```

Run frontend:

```
npm start
```

---

# Docker Setup

Build backend image:

```
docker build -t todo_backend .
```

Build frontend image:

```
docker build -t todo_frontend .
```

Run backend container:

```
docker run -d -p 3001:3001 todo_backend
```

Run frontend container:

```
docker run -d -p 3000:3000 todo_frontend
```

---

# CI/CD Pipeline

CI pipeline is configured using **GitHub Actions**.

On every push to the `main` branch:

1. Install dependencies
2. Build Docker images
3. Push images to Docker Hub

Workflow file:

```
.github/workflows/ci.yml
```

---

# Docker Hub Images

Frontend Image

```
aditya7780/todo_frontend
```

Backend Image

```
aditya7780/todo_backend
```

---

# AWS Deployment

Application is deployed on an AWS EC2 instance.

Server setup includes:

* Ubuntu Server
* Docker installed
* Containers running for frontend and backend
* MongoDB Atlas used as database

Access the application:

```
http://<EC2_PUBLIC_IP>
```

---

# Security Configuration

AWS EC2 Security Group allows:

```
HTTP  : 80
API   : 3001
SSH   : 22
```

---

# Future Improvements

* Nginx Reverse Proxy
* Automatic deployment to EC2
* Docker Compose production setup
* Kubernetes deployment
* HTTPS using SSL

---

# Author

Aditya Mandhare

GitHub
https://github.com/aditya47050

LinkedIn
[www.linkedin.com/in/aditya-mandhare-00217a26b](http://www.linkedin.com/in/aditya-mandhare-00217a26b)

---

# License

This project is open-source and available under the MIT License.
