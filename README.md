# Job Portal Application

A full‑stack **Job Portal web application** built with **MERN stack + Clerk authentication**. The platform allows users to securely authenticate, browse jobs, and manage job‑related data with a modern React (Vite) frontend and a scalable Node.js + Express backend.

---

## 🚀 Tech Stack

### Frontend (Client)

* **React 18** (Vite)
* **React Router DOM v7**
* **Tailwind CSS**
* **Axios** (API requests)
* **Clerk Authentication** (`@clerk/clerk-react`)
* **React Toastify** (notifications)
* **Quill** (rich text editor)

### Backend (Server)

* **Node.js** (ES Modules)
* **Express.js**
* **MongoDB + Mongoose**
* **Clerk (Express Middleware)**
* **JWT** (custom token usage if needed)
* **Cloudinary** (file uploads)
* **Multer** (handling multipart/form‑data)
* **Bcrypt** (password hashing – if used)
* **CORS**
* **Dotenv**
* **Sentry** (error monitoring & profiling)

---

## ✨ Features

* 🔐 Secure authentication using **Clerk**
* 👤 User session management
* 📄 Job creation & management (role‑based)
* 🧾 Rich‑text job descriptions (Quill)
* ☁️ Cloudinary file uploads
* 🔄 RESTful API architecture
* 🛡️ Protected routes (client + server)
* ⚡ Fast frontend with Vite
* 📊 Error tracking using Sentry

---

## 📁 Project Structure

```
Job-Portal/
│
├── client/               # Frontend (React + Vite)
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── vite.config.js
│
├── server/               # Backend (Node + Express)
│   ├── routes/
│   ├── models/
│   ├── controllers/
│   ├── middleware/
│   ├── lib/
│   ├── server.js
│   └── package.json
│
└── README.md
```

---

## ⚙️ Environment Variables

### Server (`server/.env`)

```
PORT=5000
MONGO_URI=your_mongodb_uri
CLIENT_URL=http://localhost:5173

CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
CLERK_WEBHOOK_SECRET=your_clerk_webhook_secret

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

SENTRY_DSN=your_sentry_dsn
NODE_ENV=development
```

### Client (`client/.env`)

```
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
VITE_API_BASE_URL=http://localhost:5000
```

---

## 🛠️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/job-portal.git
cd job-portal
```

---

### 2️⃣ Backend Setup

```bash
cd server
npm install
npm run server
```

Server runs on: **[http://localhost:5000](http://localhost:5000)**

---

### 3️⃣ Frontend Setup

```bash
cd client
npm install
npm run dev
```

Client runs on: **[http://localhost:5173](http://localhost:5173)**

---

## 🔐 Authentication Flow (Clerk)

* Frontend uses `@clerk/clerk-react`
* Backend uses `@clerk/express` middleware
* `req.auth()` is available on protected routes
* Clerk webhooks can be handled using `svix`

---

## 📡 API Overview

| Method | Route         | Description         |
| ------ | ------------- | ------------------- |
| GET    | `/health`     | Server health check |
| POST   | `/api/jobs`   | Create job          |
| GET    | `/api/jobs`   | Fetch jobs          |
| POST   | `/api/upload` | Upload files        |

*(Routes may vary based on implementation)*

---

## 🧪 Scripts

### Server

```json
"scripts": {
  "server": "nodemon server.js",
  "start": "node server.js"
}
```

### Client

```json
"scripts": {
  "dev": "vite",
  "build": "vite build",
  "preview": "vite preview"
}
```

---

## 🚀 Deployment

* **Frontend**: Vercel / Netlify
* **Backend**: Render / Railway / Fly.io
* **Database**: MongoDB Atlas

Ensure environment variables are correctly set in production.

---

## 📌 Future Improvements

* Admin dashboard
* Job application tracking
* Resume parsing
* Search & filters
* Email notifications

---

## 👤 Author

**Shreyansh Kaushal**
B.Tech Student | Full‑Stack Developer

---

## 📄 License

This project is licensed under the **ISC License**.

---

⭐ If you like this project, consider giving it a star!
