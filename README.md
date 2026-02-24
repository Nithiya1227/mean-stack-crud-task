
# MEAN Stack CRUD Application

### Dockerized Deployment on AWS EC2 with Nginx

Live Deploy Link : **http://13.233.238.236** 

## Project Summary

This project is a full-stack CRUD (Create, Read, Update, Delete) web application developed using the MEAN stack — MongoDB, Express.js, Angular, and Node.js.

The application is containerized using Docker and deployed on an AWS EC2 Ubuntu instance. Nginx is configured on the EC2 server to act as a reverse proxy, routing client requests to the appropriate Docker containers.

The project demonstrates practical experience in full-stack development, containerization, cloud deployment, and server configuration.

---

## System Architecture

The application follows a client–server model:

* The Angular frontend runs inside a Docker container.
* The Node.js + Express backend runs in a separate Docker container.
* MongoDB stores application data.
* Nginx (installed directly on the EC2 Ubuntu instance) handles incoming HTTP traffic and forwards API requests to the backend container.

### Request Flow

User → EC2 Public IP
→ Nginx (Reverse Proxy)
→ Angular Frontend Container
→ Node.js Backend Container
→ MongoDB Database

Nginx ensures the backend service is not directly exposed to the internet.

---

## Technologies Used

**Frontend**

* Angular
* TypeScript
* HTML & CSS

**Backend**

* Node.js
* Express.js

**Database**

* MongoDB

**Infrastructure & DevOps**

* Docker
* AWS EC2 (Ubuntu)
* Nginx (Reverse Proxy)

---

## Application Features

* Add new tutorial records
* Retrieve all tutorials
* Update existing tutorials
* Delete tutorials
* Search tutorials by title
* RESTful API integration between frontend and backend
* Containerized application services
* Cloud-hosted deployment

---

## Docker Implementation

Both frontend and backend services are packaged into separate Docker images.

### Build Backend Image

```bash
cd backend
docker build -t mean-backend .
```

### Build Frontend Image

```bash
cd frontend
docker build -t mean-frontend .
```

### Run Containers

```bash
docker run -d -p 5000:5000 mean-backend
docker run -d -p 80:80 mean-frontend
```

Port mappings may differ depending on your EC2 configuration.

---

## ☁ Deployment on AWS EC2

The project is deployed on an Ubuntu-based EC2 instance using the following process:

1. Launch EC2 instance
2. Configure Security Group to allow HTTP traffic (Port 80)
3. Install Docker on Ubuntu
4. Install and configure Nginx
5. Clone the repository
6. Build Docker images
7. Run containers
8. Configure Nginx reverse proxy settings

After setup, the application is accessible via the EC2 public IP address.

---

## Nginx Reverse Proxy Setup

Nginx is configured to:

* Serve the Angular frontend
* Forward API requests (for example, `/api`) to the backend container
* Handle incoming HTTP traffic securely
* Prevent direct exposure of backend service

This improves application structure and security.

---

## Project Structure

```
mean-stack-crud-task/

>backend/        # Express API and database configuration
> frontend/       # Angular client application
> Dockerfile      # Backend Docker configuration
> docker-compose.yml (optional)
> README.md
```

---

## Running the Project Locally (Without Docker)

### Backend

```bash
cd backend
npm install
node server.js
```

### Frontend

```bash
cd frontend
npm install
ng serve
```


* A clean architecture diagram explanation

Just let me know.
