<div align="center">

<img src="./frontend/public/logo.png" alt="Shorty Logo" width="120"/>

# 🚀 Shorty

### Modern URL Shortener & Link Management Platform

Fast • Secure • Scalable

<p>

<a href="http://localhost:5173">
🌐 Local Frontend
</a>
•
<a href="https://github.com/jaber-and-rafsan">
💻 Source Code
</a>

</p>

<p>

<img src="https://img.shields.io/badge/Node.js-20-339933?style=for-the-badge&logo=node.js"/>

<img src="https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react"/>

<img src="https://img.shields.io/badge/PostgreSQL-17-336791?style=for-the-badge&logo=postgresql"/>

<img src="https://img.shields.io/badge/TailwindCSS-4-38B2AC?style=for-the-badge&logo=tailwind-css"/>

<img src="https://img.shields.io/badge/License-MIT-success?style=for-the-badge"/>

</p>

</div>

---

# 📌 Overview

**Shorty** is a modern full-stack URL Shortener and Link Management Platform built with **Node.js/Express**, **React**, and **PostgreSQL**.

The platform allows authenticated users to create shortened URLs, organize and manage links through a responsive dashboard, generate QR codes, and monitor click counts. It follows a simple backend architecture, removes Redis caching, and secures all protected endpoints using JWT authentication.

Designed with scalability and simplicity in mind, Shorty demonstrates modern backend development practices while providing a clean and intuitive user experience.

---

# 🖼️ Preview

<p align="center">

<img src="./frontend/public/landing.png" width="95%"/>

</p>

<p align="center">

<img src="./frontend/public/dashboard-preview.png" width="95%"/>

</p>

<p align="center">

<img src="./frontend/public/details.png" width="95%"/>

</p>

---

# ✨ Features

## 🔐 Authentication

- User Registration
- User Login
- JWT Authentication
- Password Hashing (bcrypt)
- Protected API Routes

---

## 🔗 URL Management

- Create Short URLs
- Search URLs
- Sort URLs
- Delete URLs
- Copy URLs
- QR Code Generation
- Pagination

---

## 📊 Dashboard

- Total URLs
- Total Clicks
- Recent URLs
- URL Details
- Click Count per Link

---

## ⚡ Performance

- PostgreSQL Database
- Rate Limiting
- Optimized API Responses

---

## 🎨 User Experience

- Responsive Design
- Dark / Light Theme
- Toast Notifications
- Loading States
- Clean Modern Interface

---

# 🏗️ System Architecture

Shorty follows a layered architecture that separates business logic, request handling, and data access, making the application maintainable and scalable.

```text
                    React Frontend
                           │
                           ▼
                    REST API (Node.js/Express)
                           │
                     Middleware Layer
        (JWT • Logger • Request ID • Rate Limiter • CORS)
                           │
                           ▼
                        Handlers
                           │
                           ▼
                        Services
                           │
                           ▼
                         Stores
                   (Database Layer)
                     │
                     ▼
              PostgreSQL
```

### Architecture Layers

| Layer | Responsibility |
|------|----------------|
| Frontend | User Interface built with React |
| Middleware | Authentication, logging, rate limiting, CORS |
| Handler | Receives HTTP requests and returns responses |
| Service | Business logic |
| Store | Database operations |
| PostgreSQL | Persistent data storage |

---

# ⚙️ Technology Stack

## Frontend

- React 19
- Vite
- Tailwind CSS
- React Router DOM
- React Hot Toast
- React Icons

---

## Backend

- Node.js / Express
- JWT Authentication
- REST API

---

## Database

- PostgreSQL

---

## Local Development

- Frontend: http://localhost:5173
- Backend: http://localhost:8080

---


# 📂 Project Structure

```text
Shorty
│
├── backend
│   ├── db
│   ├── db.js
│   ├── entrypoint.sh
│   ├── index.js
│   ├── migrate.js
│   ├── package.json
│   └── .env.example
│
├── frontend
│   ├── public
│   ├── src
│   │   ├── api
│   │   ├── assets
│   │   ├── components
│   │   ├── context
│   │   ├── hooks
│   │   ├── pages
│   │   └── utils
│   │
│   ├── package.json
│   └── vite.config.js
│
└── README.md
```

---

# 🚀 Core Features

- 🔐 JWT Authentication
- 🔗 URL Shortening
- 📊 Click Counting
- 📱 Responsive Dashboard
- 🌙 Dark / Light Theme
- 🔍 Search & Sorting
- 📄 Pagination
- 📋 Copy to Clipboard
- 📱 QR Code Generation
- 🗑️ URL Deletion

---

# 🔄 Request Flow

```text
User
 │
 ▼
React Frontend
 │
 ▼
Node.js/Express REST API
 │
 ▼
Authentication Middleware
 │
 ▼
Business Logic
 │
 ▼
PostgreSQL
 │
 ▼
JSON Response
 │
 ▼
Frontend
```

---

# ⚙️ Getting Started

## Prerequisites

Before running the project, make sure you have the following installed:

- Node.js 20+
- PostgreSQL
- Git

---

# 📥 Installation

## Clone the repository

```bash
git clone https://github.com/jaber-and-rafsan/Shorty.git
cd Shorty
```

---

## Backend Setup

```bash
cd backend
npm install
npm run migrate
npm start
```

The backend will start on:

```
http://localhost:8080
```

---

## Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

The frontend will start on:

```
http://localhost:5173
```

---

# 🔑 Environment Variables

Create a `.env` file inside the **backend** directory.

```env
PORT=8080
DATABASE_URL=postgres://username:password@localhost:5432/shorty?sslmode=disable
JWT_SECRET=your_secret_key
BASE_URL=http://localhost:8080
CORS_ORIGINS=http://localhost:5173,http://127.0.0.1:5173
```

---

# 📖 API Reference

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | `/register` | Register a new user |
| POST | `/login` | Authenticate user |
| POST | `/shorten` | Create a short URL |
| GET | `/r/{id}` | Redirect to original URL |
| GET | `/user/urls` | Get all user URLs |
| DELETE | `/user/urls/{id}` | Delete a URL |

---

#  Deployment

| Service | Platform |
|----------|----------|
| Frontend | Local Development |
| Backend | Local Development |
| Database | PostgreSQL |

---

# 🛣️ Roadmap

## ✅ Completed

- JWT Authentication
- URL Shortening
- Click Tracking
- Dashboard
- URL Details
- QR Code Generation
- Search URLs
- Sort URLs
- Pagination
- Rate Limiting
- Responsive Design
- Dark / Light Theme

---

## 🔮 Planned Features

- Custom URL Aliases
- Link Expiration
- Advanced Click Analytics
- Geographic Analytics
- Device Analytics
- Export Reports
- Team Workspaces
- Admin Dashboard

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature/your-feature
```

3. Commit your changes

```bash
git commit -m "Add new feature"
```

4. Push to your branch

```bash
git push origin feature/your-feature
```

5. Open a Pull Request

---

# 👨‍💻 Authors

**Jaber & rafsan**

- GitHub: https://github.com/jaber-and-rafsan

---

# ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub.

It helps others discover the project and motivates future development.

---

# 📄 License

This project is licensed under the MIT License.

See the `LICENSE` file for more information.
