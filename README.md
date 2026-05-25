# URL Shortener API

[![Node.js](https://img.shields.io/badge/Node.js-Backend-green)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express.js-Framework-black)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Database-green)](https://www.mongodb.com/)
[![Docker](https://img.shields.io/badge/Docker-Enabled-blue)](https://www.docker.com/)
[![REST API](https://img.shields.io/badge/API-REST-orange)](#)

A scalable URL shortening service built with **Node.js** and **Express.js**.

This project allows users to convert long URLs into short, shareable links while demonstrating backend engineering concepts such as REST API development, database persistence, Dockerization, validation, and scalable backend architecture.

---

# Repository

* GitHub Repository: [URL-Shortener Repository](https://github.com/Bashiru09/URL-Shortener.git?utm_source=chatgpt.com)

---

# Features

## URL Shortening

* Generate short URLs from long links
* Unique short code generation
* Redirect shortened URLs to original destinations

## Backend Features

* RESTful API design
* Request validation
* Error handling middleware
* Clean project structure
* Environment-based configuration

## Database & Persistence

* Store shortened URLs persistently
* Efficient URL lookup
* Scalable backend design

## Developer Experience

* Dockerized setup
* Easy local development
* Modular architecture

---

# Tech Stack

## Backend

* Node.js
* Express.js

## Database

* MongoDB

## DevOps & Tooling

* Docker
* Docker Compose

## Utilities

* dotenv
* nodemon

---

# Architecture

The application follows a layered backend architecture:

```text id="qpr06d"
Routes → Controllers → Services → Database
```

This structure improves:

* maintainability
* scalability
* separation of concerns
* easier testing

---

# How It Works

## URL Shortening Flow

```text id="jlwm1j"
User submits long URL
        ↓
Server generates short code
        ↓
Short URL stored in database
        ↓
Short URL returned to user
        ↓
Visiting short URL redirects to original URL
```

---

# API Endpoints

## Create Short URL

| Method | Endpoint   | Description            |
| ------ | ---------- | ---------------------- |
| POST   | `/shorten` | Generate shortened URL |

### Example Request

```json id="jlwmfx"
{
  "url": "https://example.com/some/very/long/url"
}
```

### Example Response

```json id="w2bl9w"
{
  "shortUrl": "http://localhost:3000/abc123"
}
```

---

## Redirect URL

| Method | Endpoint      | Description              |
| ------ | ------------- | ------------------------ |
| GET    | `/:shortCode` | Redirect to original URL |

---

# Project Structure

```text id="xowk9s"
src/
├── controllers/
├── routes/
├── services/
├── models/
├── middleware/
├── config/
└── utils/
```

---

# Local Setup

## Clone Repository

```bash id="yrkv10"
git clone https://github.com/Bashiru09/URL-Shortener.git
cd URL-Shortener
```

---

## Install Dependencies

```bash id="jlwmz1"
npm install
```

---

## Configure Environment Variables

Create a `.env` file:

```env id="jlwm2x"
PORT=3000
MONGO_URI=
BASE_URL=http://localhost:3000
```

---

## Run Development Server

```bash id="jlwm3y"
npm run dev
```

Application runs at:

```text id="jlwm4z"
http://localhost:3000
```

---

# Docker Setup

Run with Docker:

```bash id="jlwm5a"
docker compose up --build
```

---

# Example Use Case

Input:

```text id="jlwm6b"
https://www.example.com/articles/backend-engineering
```

Output:

```text id="jlwm7c"
http://localhost:3000/aB12xY
```

---

# Future Improvements

* Custom aliases
* URL expiration
* Click analytics
* QR code generation
* Redis caching
* Rate limiting
* Authentication & user accounts
* AWS deployment
* Monitoring & logging

---

# What I Learned

This project strengthened my understanding of:

* Node.js backend development
* Express middleware architecture
* REST API design
* database modeling
* Docker workflows
* scalable backend structure

---

# Author

Built by [Bashiru09 GitHub Profile](https://github.com/Bashiru09?utm_source=chatgpt.com)

Backend Engineer focused on:

* Node.js & Express
* Cloud & DevOps
* Backend Architecture
* Scalable APIs
