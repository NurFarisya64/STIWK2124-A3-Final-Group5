# 📚 Accessible Reading List (ARL)

## Full-Stack Containerized Web Application Using Docker

### Course Information

| Item       | Details                                                               |
| ---------- | --------------------------------------------------------------------- |
| Course     | STIWK2124 Web Engineering                                             |
| Semester   | A252 – February 2025/2026                                             |
| Assignment | Assignment 3 – CLO3: Full-Stack Containerized Deployment Using Docker |
| Lecturer   | Dr. Munya Saleh Saeed Ba Matraf                                       |

---

# 📖 Project Overview

Accessible Reading List (ARL) is a modern full-stack web application developed to manage a digital reading list through a user-friendly interface and secure RESTful services.

The system is built using Angular, Spring Boot, and MySQL, and fully deployed using Docker Compose. All application components are containerized and connected through a dedicated Docker network, enabling easy deployment, scalability, portability, and consistent execution across different environments.

The application allows users to efficiently manage books through Create, Read, Update, and Delete (CRUD) operations while ensuring a seamless user experience.

---

# 🎯 System Objectives

The ARL system is designed to:

* Provide a centralized platform for managing reading materials
* Demonstrate full-stack web application development
* Implement RESTful API communication between frontend and backend
* Apply containerization technologies using Docker
* Enable one-command deployment using Docker Compose
* Demonstrate microservices architecture principles

---

# ✨ Key Features

### Book Management

* View complete book collection
* Search books by title or author
* Add new books
* Edit existing book information
* Delete books
* Real-time data updates

### User Experience

* Responsive user interface
* Form validation
* Error handling and feedback messages
* Search and filtering functionality
* Pagination support

### DevOps Features

* Dockerized deployment
* Multi-container architecture
* Persistent database storage
* Internal Docker networking
* Nginx reverse proxy
* One-command application startup

---

# 🛠 Technology Stack

## Frontend Layer

| Technology         | Purpose               |
| ------------------ | --------------------- |
| Angular 17+        | Frontend Framework    |
| TypeScript         | Application Logic     |
| HTML5              | Structure             |
| CSS3               | Styling               |
| Bootstrap 5        | Responsive Design     |
| Angular HttpClient | API Communication     |
| Nginx              | Production Web Server |

---

## Backend Layer

| Technology      | Purpose               |
| --------------- | --------------------- |
| Spring Boot     | REST API Development  |
| Spring Data JPA | Data Access Layer     |
| Hibernate       | ORM Framework         |
| Maven           | Dependency Management |
| MySQL Driver    | Database Connectivity |

---

## Database Layer

| Technology    | Purpose                 |
| ------------- | ----------------------- |
| MySQL 8.x     | Relational Database     |
| Docker Volume | Persistent Data Storage |

---

## DevOps & Tools

| Technology         | Purpose                 |
| ------------------ | ----------------------- |
| Docker             | Containerization        |
| Docker Compose     | Service Orchestration   |
| GitHub             | Version Control         |
| Postman            | API Testing             |
| Visual Studio Code | Development Environment |

---

# 🏗 System Architecture

The application follows a three-tier microservices architecture deployed using Docker containers.

Frontend Layer (Angular + Nginx)
↓
Backend Layer (Spring Boot REST API)
↓
Database Layer (MySQL)

### Services

#### 1. frontend-service

Responsibilities:

* Display user interface
* Handle user interactions
* Consume REST APIs
* Serve Angular production build through Nginx

Port:
80

---

#### 2. backend-service

Responsibilities:

* Business logic processing
* REST API endpoints
* Data validation
* Database interaction

Port:
8080

---

#### 3. db-service

Responsibilities:

* Persistent storage
* Book record management

Port:
Internal Docker Network Only

---

# 🐳 Docker Deployment

## Prerequisites

Install Docker Desktop:

https://www.docker.com/products/docker-desktop/

Verify installation:

```bash
docker --version
docker compose version
```

---

# 🚀 Getting Started

## Step 1: Clone Repository

```bash
git clone https://github.com/NurFarisya64/STIWK2124-A3-Final-Group5.git
cd ARL-Library-Project
```

---

## Step 2: Build and Start All Services

```bash
docker compose up -d --build
```

This command will:

* Build Angular frontend image
* Build Spring Boot backend image
* Download MySQL image
* Create Docker network
* Start all containers
* Configure inter-service communication

---

## Step 3: Verify Running Containers

```bash
docker ps
```

Expected containers:

```text
frontend-service
backend-service
db-service
```

---

## Step 4: Access Application

### Frontend Application

```text
http://localhost/books
```

### Backend API

```text
http://localhost:8080/api/books
```

### Database

```text
MySQL Database (Internal Docker Network)
```

---

# 🔗 API Integration

The Angular frontend communicates with the Spring Boot backend through:

```text
http://localhost/api/books
```

## Supported Endpoints

| Method | Endpoint        | Description              |
| ------ | --------------- | ------------------------ |
| GET    | /api/books      | Retrieve all books       |
| GET    | /api/books/{id} | Retrieve a specific book |
| POST   | /api/books      | Create a new book        |
| PUT    | /api/books/{id} | Update book information  |
| DELETE | /api/books/{id} | Delete a book            |

---

# 💾 Data Persistence

The MySQL database uses Docker Volumes to ensure data remains available even after containers are stopped or restarted.

Benefits:

* Persistent storage
* Data protection
* Easy backup and recovery
* Container-independent database lifecycle

---

# 🔧 Docker Features Implemented

✅ Full Application Containerization

✅ Multi-Service Docker Compose Setup

✅ Internal Docker Network Communication

✅ Nginx Reverse Proxy Configuration

✅ Persistent MySQL Volume Storage

✅ Automated Service Dependency Management

✅ Environment Variable Configuration

✅ One-Command Deployment

---

# 📋 Useful Docker Commands

### Start Services

```bash
docker compose up -d
```

### Rebuild and Start

```bash
docker compose up -d --build
```

### Stop Services

```bash
docker compose down
```

### View Running Containers

```bash
docker ps
```

### View Logs

```bash
docker compose logs -f
```

### Rebuild Frontend Only

```bash
docker compose up --build frontend-service
```

### Rebuild Backend Only

```bash
docker compose up --build backend-service
```

### Complete Clean Restart

```bash
docker compose down
docker compose up -d --build
```

---

# 📈 Learning Outcomes Achieved

This project demonstrates:

* Full-stack web development
* RESTful API design
* Frontend-backend integration
* Database management
* Docker containerization
* Docker Compose orchestration
* Microservices deployment
* Production-ready application deployment practices

---

# 👥 Group Members

| Name                                    | Matric Number |
| --------------------------------------- | ------------- |
| NUR FARISYA BINTI AHMAD SHUKRI          | 303383        |
| NUR JUWANA BINTI MOHD YUNUS             | 307909        |
| SITI NUR IRDINA BINTI AHMAD SUKARDI     | 307504        |
| ALIYYAH SAFIAH BINTI HAZLY              | 305604        |
| NUR SYATHIRAH BINTI MOHD FAIZATUL IZHAM | 305766        |

---

# 📌 Quick Start Summary

```bash
# Clone Repository
git clone https://github.com/NurFarisya64/STIWK2124-A3-Final-Group5.git

# Enter Project Directory
cd ARL-Library-Project

# Build and Run Containers
docker compose up -d --build

# Open Application
http://localhost/books
```

---

# 📄 License

This project was developed solely for educational purposes under the STIWK2124 Web Engineering course at Universiti Utara Malaysia (UUM).

