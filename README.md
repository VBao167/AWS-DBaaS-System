# ☁️ AWS Database-as-a-Service (DBaaS) Provisioning System

## 📌 Project Overview
An automated Database-as-a-Service (DBaaS) platform designed to allow end-users to dynamically provision, manage, and delete isolated MySQL databases. This project demonstrates a solid understanding of Cloud Infrastructure (AWS) and automated database management workflows.

## 🛠️ Technology Stack
* **Cloud Infrastructure:** Amazon Web Services (AWS) - RDS (MySQL), EC2
* **Backend:** Python, Django REST Framework (DRF)
* **Frontend:** HTML5, CSS3 (Bootstrap 5), Vanilla JavaScript
* **Database:** MySQL
* **Security & Auth:** JSON Web Tokens (JWT)

## ⚙️ Core System Architecture
This project utilizes a 3-tier architecture to ensure separation of concerns and security:
1.  **Presentation Layer:** A responsive web dashboard allowing users to interact with the system without needing raw SQL queries.
2.  **Application Layer (API):** Django REST Framework handles business logic, user authentication (JWT), and executes dynamic MySQL provisioning scripts via `mysql-connector-python`.
3.  **Data Layer:** AWS RDS serves as the central database engine. When a user requests a new database, the API dynamically executes `CREATE DATABASE` and `GRANT PRIVILEGES` commands on the RDS instance to create an isolated environment.

## 🚀 Key Features
* **Dynamic Database Provisioning:** Users can request a new database with a custom password instantly.
* **Automated Privilege Management:** The system automatically generates a unique MySQL user for each new database and grants strict, isolated privileges.
* **Secure Authentication:** Implemented JWT (JSON Web Tokens) for secure API communication.
* **Resource Lifecycle Management:** Users can view their active databases and securely drop (delete) them when no longer needed.

## 🧠 What I Learned
Through this project, I gained hands-on experience with:
* Configuring and connecting to AWS RDS instances.
* Writing programmatic SQL execution scripts in Python.
* Designing RESTful APIs and managing state with JWT.
* Structuring database automation workflows.
