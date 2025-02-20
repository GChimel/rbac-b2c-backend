# 📌 RBAC - B2C - BACKEND

This repository demonstrates how to implement **Role-Based Access Control (RBAC)** in a **Business-to-Consumer (B2C)** system where users cannot create new roles.

## 🚀 What is RBAC?

**Role-Based Access Control (RBAC)** is a security model used to manage permissions within a system. Instead of assigning permissions to individual users, they are assigned to predefined roles. This simplifies access management, enhances security, and ensures compliance.

### 🛠 How RBAC Works in This Project

- Accounts are assigned to predefined roles.
- Roles have specific permissions, controlling what actions account can perform.
- A account cannot create or modify roles; only system administrators can manage them.

## 🏗 Tech Stack

- **Node.js** – Backend runtime
- **Express** – Web framework
- **TypeScript** – Strongly typed JavaScript
- **Prisma** – ORM for database management
- **PostgreSQL** – Relational database
- **Docker Compose** – Containerized environment

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```sh
git clone https://github.com/GChimel/rbac-b2c-backend.git
cd rbac-b2c-backend
```

### 2️⃣ Install Dependencies

```sh
yarn
```

### 3️⃣ Create a .env file in the root of the app

- DATABASE_URL="pgconnectionstring"
- JWT_SECRET="jwtsecretkey"

### 4️⃣ Start Services with Docker

Ensure **Docker** and **Docker Compose** are installed. Then run:

```sh
docker-compose up -d
```

### 5️⃣ Run Migrations

```sh
npx prisma migrate dev
```

### 6️⃣ Start the Server

```sh
yarn dev
```

## 🔑 Endpoints Overview

### 🧑‍💻 Authentication

- `POST /sign-in` – Authenticate user and return token.

### 👤 Account Management

- `POST /sign-up` – Create a new account.
  - By default role = "USER"

### 🔒 Role Management

- `GET /leads` – List an example of leads.

  - All roles can see use this rote

- `POST/leads`- (Private) - Example of create a lead.
  - Just role "ADMIN" can create.

## 📜 License

This project is licensed under the MIT License.
