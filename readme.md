# Blog WebApp – Auth + Blog (CRUD + SSR)

A **Blog Web Application** built with **Node.js, Express, MongoDB, and EJS**.  
It demonstrates **Authentication, Blog & Comment CRUD operations, and Server-Side Rendering (SSR)** with a clean, maintainable structure.

---

## Live Demo

[BlogNest v1 – Deployed App](http://blognest-v1.ap-south-1.elasticbeanstalk.com/)

---

## Features

- **Authentication**
- User signup & login with secure password hashing via **bcrypt**
- **Session-based authentication** (express-session + cookies) and protected routes

- **Blog CRUD**
- Create, read, update, and delete blog posts
- Posts are linked to registered users

- **Comment System**
- Add, edit, and delete your own comments
- View all comments under a blog

- **Server-Side Rendering (SSR)**
- EJS views with layouts/partials
- Flash messages for feedback

- **Middleware**
- Auth guard for protected routes
- Error handling
- Method-override for PUT & DELETE in forms

---

## Tech Stack

- **Backend:** Node.js, Express.js
- **Database:** MongoDB + Mongoose
- **Templating Engine:** EJS
- **Authentication:** Json Webtoken
- **Other:** dotenv, connect-flash, method-override

---

## Project Structure

```

blog-webapp-auth-crud-ssr/
│── controllers/        # Business logic for blogs, comments, auth
│── middlewares/        # Auth & error middleware
│── models/             # Mongoose schemas (User, Blog, Comment)
│── routes/             # Express routes (auth, blogs, comments)
│── services/           # Reusable helpers
│── views/              # EJS templates (layouts, partials, pages)
│── public/             # Static assets (CSS, JS, images)
│── index.js            # Entry point
│── package.json        # Dependencies
│── .env                # Environment variables

```

---

## Installation & Setup

### 1) Clone

```bash
git clone https://github.com/hamzanazir27/blog-webapp-auth-crud-ssr.git
cd blog-webapp-auth-crud-ssr
```

### 2) Install

```bash
npm install
```

### 3) Configure Environment Variables

Create a `.env` file:

```
PORT=5000
MONGO_URI=your_mongo_db_connection_string
SESSION_SECRET=your_session_secret
```

### 4) Run

```bash
npm start
```

Now open [http://localhost:5000](http://localhost:5000)

---

## Routes Overview

### Auth

- `GET /auth/login` – Login page
- `POST /auth/login` – Authenticate user
- `GET /auth/signup` – Signup page
- `POST /auth/signup` – Register new user
- `GET /auth/logout` – Logout and destroy session

### Blogs

- `GET /blogs` – List all blogs
- `GET /blogs/new` – Create blog form
- `POST /blogs` – Create blog
- `GET /blogs/:id` – View blog details
- `GET /blogs/:id/edit` – Edit blog
- `PUT /blogs/:id` – Update blog _(via method-override)_
- `DELETE /blogs/:id` – Delete blog _(via method-override)_

### Comments

- `POST /blogs/:id/comments` – Add a comment
- `GET /blogs/:id/comments/:commentId/edit` – Edit comment form
- `PUT /blogs/:id/comments/:commentId` – Update comment _(via method-override)_
- `DELETE /blogs/:id/comments/:commentId` – Delete comment _(via method-override)_

---

## Contributing

Issues and PRs are welcome! Please open an issue to discuss major changes before submitting.

---
