
---

# MEAN Stack CRUD Application

This repository contains a full-stack web application built using the **MEAN stack** — *MongoDB, Express.js, Angular 15, and Node.js* — that supports Create, Read, Update, and Delete (CRUD) operations for managing tutorials. The backend offers REST APIs using **Node.js** and **Express**, while the frontend is developed with **Angular** and communicates with the server using Angular’s `HttpClient`.

## Project Overview

This application allows users to perform the following core tasks:

* **Create** new tutorials with title and description.
* **Read** and list all tutorials stored in the database.
* **Update** the details of an existing tutorial.
* **Delete** single or multiple tutorials.
* **Search** tutorials by title.

The goal of this project is to demonstrate a working full-stack solution using a popular JavaScript stack that handles data persistence, API development, and frontend interaction.

## Tech Stack

This application leverages the following technologies:

* **MongoDB** — A NoSQL database for storing tutorial records.
* **Express.js** — Backend framework to build RESTful APIs.
* **Angular 15** — Frontend framework for building the UI and handling data interaction.
* **Node.js** — Runtime environment for executing the backend.

## Features

✔ Angular frontend with a responsive user interface
✔ REST API endpoints for tutorial management
✔ Search tutorials by title
✔ CRUD operations fully implemented
✔ Client-server communication using HTTP requests

## Project Structure

```
/
├── backend/         # Express/Node.js API server
├── frontend/        # Angular 15 application
├── docker-compose.yml
└── README.md        # Documentation
```

## 🛠 Prerequisites

Before running the project, ensure the following are installed:

* Node.js (v14 or higher)
* npm (Node Package Manager)
* Angular CLI (for frontend)
* MongoDB (running locally or MongoDB Atlas configured)

## How to Run

### 1. Backend (API Server)

```bash
cd backend
npm install
# Set your MongoDB connection configs in `db.config.js`
node server.js
```

### 2. Frontend (Angular Client)

```bash
cd frontend
npm install
ng serve --port 8081
```

Once both backend and frontend are running, open your browser and navigate to:

http://13.233.238.236/

1.Project Configuration

* You can update the MongoDB credentials in the backend config file.
* To modify how the Angular app interacts with the backend, adjust service files like `tutorial.service.ts`.
2.Contributing

Contributions are welcome! Feel free to submit pull requests or open issues if you find bugs, need help, or want to suggest improvements.


