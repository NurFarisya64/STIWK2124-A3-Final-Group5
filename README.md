**📚 Accessible Reading List (ARL) — Dockerized Full-Stack System**

**Course Information**
**Course:** STIWK2124 Web Engineering
**Semester:** A252 – Feb 2025/2026
**Assignment:** Assignment 3 — CLO3: Full-Stack Containerized Deployment Using Docker
**Lecturer:** Dr. Munya Saleh Saeed Ba Matraf

**Project Overview**
Accessible Reading List (ARL) is a full-stack containerized web application developed using Angular, Spring Boot, and MySQL, fully orchestrated using Docker Compose.

This project extends previous assignments by deploying the entire system as microservices using containers.

The system allows users to:

* View book list
* Search books
* Add books
* Edit books
* Delete books
* Validate forms
* Run the entire system using Docker (one command deployment)

**Technologies Used**
**Frontend**
* Angular (v17+ Standalone Components)
* TypeScript
* HTML / CSS
* Bootstrap
* Angular HttpClient
* Nginx (production build server)
  
**Backend**
* Spring Boot (REST API)
* Spring Data JPA
* Hibernate
* MySQL Driver
  
**Database**
* MySQL 8.x (Docker container)
  
**DevOps / Tools**
* Docker
* Docker Compose
* Visual Studio Code
* GitHub
* Postman

**System Architecture**
The system consists of 3 microservices connected via Docker network:
**1. frontend-service**
* Angular application
* Built and served using Nginx
* Runs on port 80
**2. backend-service**
* Spring Boot REST API
* Runs on port 8080
* Handles all business logic
**3. db-service**
* MySQL database
* Stores all book records
* Internal Docker network only (not exposed)

**Docker Setup (Prerequisites)**
Before running this project, ensure:
* Docker Desktop is installed
https://www.docker.com/products/docker-desktop/
* Docker Compose is enabled (included in Docker Desktop)
Verify installation:
docker --version
docker compose version

**How to Run the Project (Docker Deployment)**
**1. Clone the Repository**
git clone <your-repository-link>
cd ARL-Library-Project

**2. Build and Run All Services**
docker compose up -d --build

* This command will:
* Build Angular frontend image
* Build Spring Boot backend image
* Pull MySQL image
* Start all containers
* Connect services using Docker network

**3. Check Running Containers**
docker ps

**4. Stop the System**
docker compose down

**Application Access**
Once containers are running:
📚 Frontend (Angular UI):
http://localhost/books
🔌 Backend API:
http://localhost:8080/api/books
🗄️ MySQL Database:
Runs internally inside Docker (not exposed)

**API Integration**
The Angular frontend communicates with Spring Boot backend via:
http://localhost/api/books

**API Methods:**
* GET → Retrieve books
* POST → Add books
* PUT → Update books
* DELETE → Delete books

**Docker Features Implemented**
* Full microservices containerization
* Docker Compose orchestration
* Internal Docker network communication
* Nginx reverse proxy for frontend routing
* MySQL persistent volume storage
* One-command deployment (docker compose up -d --build)

**Useful Docker Commands**
**Rebuild frontend only**
docker compose up --build frontend-service

**Rebuild backend only**
docker compose up --build backend-service

**View logs**
docker compose logs -f

**Clean restart system**
docker compose down && docker compose up -d --build

**Features Implemented**
* Full CRUD operations
* Search & filtering
* Pagination support
* Form validation
* REST API integration
* Dockerized deployment
* Nginx reverse proxy setup
* MySQL persistence with volume
* Fully isolated microservices architecture

**Group Members**
* NUR FARISYA BINTI AHMAD SHUKRI	303383
* NUR JUWANA BINTI MOHD YUNUS	307864
* SITI NUR IRDINA BINTI AHMAD SUKARDI	307504
* ALIYYAH SAFIAH BINTI HAZLY	305604
* NUR SYATHIRAH BINTI MOHD FAIZATUL IZHAM	305766

**How to Run Summary**
1. Install Docker
2. Clone project
3. Run:
docker compose up -d --build
4. Open:
http://localhost/books

**License**
This project is developed for educational purposes under STIWK2124 Web Engineering.
