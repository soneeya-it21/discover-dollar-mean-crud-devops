📘 Discover Dollar – MEAN CRUD DevOps Project
Full-Stack CRUD Application + Docker + Nginx + GitHub Actions CI/CD

This project implements a MEAN-stack (MongoDB, Express, Angular, Node.js) CRUD application deployed using Docker Compose, reverse-proxied using Nginx, and automated using GitHub Actions CI/CD.

It includes the full workflow:

1) Frontend Angular application
2) Backend REST API using Node.js + Express
3) MongoDB database
4) Nginx reverse proxy
5) Dockerized multi-container setup
6) CI/CD pipeline for automated build, test, Docker push, and server deployment


🚀 Project Architecture
┌────────────────────────┐
│        Angular         │
│     (Frontend UI)      │
└───────────┬────────────┘
            │ /api/ calls
┌───────────▼────────────┐
│     NGINX Reverse      │
│         Proxy          │
└───────────┬────────────┘
     /api   │   /
┌───────────▼────────────┐
│   Node.js Backend API  │
└───────────┬────────────┘
            │ Mongoose
┌───────────▼────────────┐
│       MongoDB          │
└────────────────────────┘


🛠️ Tech Stack

Component	                                                                  Technology
Frontend	                     ----->                                         Angular
Backend	                       ----->                                     Node.js + Express
Database	                     ----->                                         MongoDB
Reverse Proxy	                 ----->                                          Nginx
Containerization	             ----->                                   Docker & Docker Compose
CI/CD	                         ----->                                      GitHub Actions
Hosting	                       ----->                                     AWS EC2 (Ubuntu)


📂 Features Implemented

✔ Full CRUD Operations
- Create Tutorial
- Fetch all Tutorials
- View Tutorial Details
- Update Tutorial
- Delete Tutorial
- Delete All Tutorials

✔ Nginx Reverse Proxy
- Serves Angular frontend
- Proxies /api/** to backend
- Clean URLs (no port numbers exposed)

✔ Dockerized Multi-Service App
- mean-frontend
- mean-backend
- mean-mongo
- mean-nginx

✔ GitHub Actions CI/CD
- Automatically triggers on every push
- Builds Angular & Node.js
- Builds Docker images
- Pushes to Docker Hub
- SSH deploy script updates EC2 automatically


📦 Docker Compose Setup
 
Start Application
----docker compose up --build -d
Stop Application
----docker compose down
Verify Running Containers
----docker ps 


🌐 Application URLs

Component	                                      URL
Frontend	           ------                http://<EC2-IP>
Tutorials Page	     ------                  /tutorials
Add Tutorial	       ------                     /add 
API Test	           ------           http://<EC2-IP>/api/tutorials


🧪 API Endpoints (Backend)

Method	                                    Endpoint	                                          Description
POST	                                    /api/tutorials	                                   Create a tutorial
GET	                                      /api/tutorials	                                   List all tutorials
GET	                                      /api/tutorials/:id	                                Get one tutorial
PUT	                                      /api/tutorials/:id	                                Update tutorial
DELETE	                                  /api/tutorials/:id	                                 Delete tutorial
DELETE	                                  /api/tutorials	                                   Delete all tutorials



🔁 CI/CD Pipeline (GitHub Actions)

Pipeline stages:
1)Checkout repository
2)Install dependencies (Node & Angular)
3)Run frontend and backend builds
4)Build Docker images
5)Push to Docker Hub
6)SSH into EC2
7)Pull latest images
8)Restart Docker Compose
9)This ensures zero manual deployment.


🖼️ Required Submission Screenshots

📌 Application Functionality
![Add](https://github.com/user-attachments/assets/121ff205-395a-4e60-bbc8-1a7f7d619265)
![Tutorial](https://github.com/user-attachments/assets/08e982ee-aeb4-4ab0-9014-0c7cd8fe39ea)
![Edit](https://github.com/user-attachments/assets/3adfd1bf-86bb-42ec-a4c0-955292ea826c)
![Delete](https://github.com/user-attachments/assets/2df68cb7-95f8-420f-b7c0-ca7a89e78d9d)

📌 Docker & Backend Verification
![Docker compose and logs](https://github.com/user-attachments/assets/09184965-f5eb-439f-bac3-6d201f9b0b9b)
![showing response](https://github.com/user-attachments/assets/618f2d55-a01d-43d1-bd8e-8daccbe436d7)
![Docker Frontend image](https://github.com/user-attachments/assets/605eac2f-aea7-4b9b-962d-43ee83ece5b7)
![Docker backend image](https://github.com/user-attachments/assets/aaec3377-8f3f-4de2-86b9-5d608b159198)

📌 NGINX Verification
![API calling](https://github.com/user-attachments/assets/fb135c06-2e18-4591-9754-86c8a7efd4f4)

📌 GitHub Actions CI/CD
![WorkFlow](https://github.com/user-attachments/assets/c60a89f3-b461-4f36-9294-c5055538a4f7)
![Builds](https://github.com/user-attachments/assets/23772130-143d-41ff-bec4-dd5c8d09cbe0)
![build and Push](https://github.com/user-attachments/assets/dda5da8f-ff07-4ae6-871c-76bce2223f1d)
![deploy ](https://github.com/user-attachments/assets/b03f2513-9990-45a6-aa04-a7a60dbe08cc)


📜 Project Folder Structure

discover-dollar-mean-crud-devops/
 ├── crud-dd-task-mean-app/
 │   ├── backend/
 │   ├── frontend/
 │   ├── nginx/
 │   ├── docker-compose.yml
 │   └── README.md


📘 Conclusion

This project demonstrates:
✔ MEAN full-stack development
✔ Containerized microservices
✔ Reverse proxy with Nginx
✔ Cloud deployment using Docker
✔ Fully automated CI/CD with GitHub Actions

This setup makes the application production-ready, scalable, and easily maintainable.
