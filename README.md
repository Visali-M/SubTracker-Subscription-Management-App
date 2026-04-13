# 📊 SubTracker — Subscription Management App

A full-stack **MERN application** to track, manage, and pay for all your recurring subscriptions in one place.

---

## 🚀 Features

* 🔐 **User Authentication** — Register & Login using JWT
* ➕ **Add Subscriptions** — Smart cascading dropdowns (Category → Service → Plan)
* ✏️ **Edit & Delete** — Full CRUD operations for subscriptions
* 💳 **Razorpay Payments** — Pay subscriptions directly from the dashboard
* 📊 **Analytics Dashboard**

  * Spending by category
  * Monthly trends
  * Distribution charts
* 🔔 **Renewal Alerts** — Notifications for upcoming renewals
* ⏰ **Cron Jobs** — Daily automated renewal reminders
* 👤 **Profile Management** — Update name, email, password
* ⚙️ **Settings Panel** — Notification preferences, currency, danger zone

---

## 🛠️ Tech Stack

### 🔹 Frontend

| Technology        | Purpose             |
| ----------------- | ------------------- |
| React 18          | UI Framework        |
| React Router v6   | Page Routing        |
| Axios             | API Requests        |
| DM Sans + DM Mono | Typography          |
| Chart.js          | Data Visualization  |
| Razorpay SDK      | Payment Integration |

### 🔹 Backend

| Technology         | Purpose          |
| ------------------ | ---------------- |
| Node.js + Express  | REST API Server  |
| MongoDB + Mongoose | Database         |
| JWT                | Authentication   |
| bcryptjs           | Password Hashing |
| Razorpay           | Payment Gateway  |
| node-cron          | Scheduled Jobs   |

---

## 📁 Project Structure

```
subscription-tracker/
├── backend/
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   ├── authController.js
│   │   └── subscriptionController.js
│   ├── middleware/
│   │   └── authMiddleware.js
│   ├── models/
│   │   ├── User.js
│   │   └── Subscription.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── subscriptionRoutes.js
│   │   └── paymentRoutes.js
│   ├── utils/
│   │   └── cronJob.js
│   ├── .env
│   ├── server.js
│   └── package.json
│
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── App.js
│   │   └── App.css
│   ├── .env
│   └── package.json
│
├── .gitignore
└── README.md
```

---

## ⚙️ Installation & Setup

### 🔧 Prerequisites

* Node.js (v16+)
* MongoDB (Local or Atlas)
* Razorpay account (Test mode)

---

### 1️⃣ Clone Repository

```
git clone https://github.com/yourusername/subscription-tracker.git
cd subscription-tracker
```

---

### 2️⃣ Backend Setup

```
cd backend
npm install
```

Create `.env` file:

```
PORT=5000
MONGO_URI=mongodb://localhost:27017/subscription-tracker
JWT_SECRET=your_super_secret_jwt_key
RAZORPAY_KEY_ID=rzp_test_XXXXXXXXXXXX
RAZORPAY_KEY_SECRET=XXXXXXXXXXXX
CLIENT_URL=http://localhost:3000
```

Start backend:

```
npm run dev
```

👉 Runs on: http://localhost:5000

---

### 3️⃣ Frontend Setup

```
cd frontend
npm install
```

Create `.env` file:

```
REACT_APP_API_URL=http://localhost:5000/api
REACT_APP_RAZORPAY_KEY=rzp_test_XXXXXXXXXXXX
```

Start frontend:

```
npm start
```

👉 Runs on: http://localhost:3000

---

## 🔑 Razorpay Setup

1. Go to: https://dashboard.razorpay.com
2. Login / Sign up
3. Navigate to **Settings → API Keys**
4. Generate Test Key
5. Copy:

   * Key ID → frontend + backend
   * Key Secret → backend only

---

## 📡 API Endpoints

### 🔐 Authentication

| Method | Endpoint           | Description    |
| ------ | ------------------ | -------------- |
| POST   | /api/auth/register | Register user  |
| POST   | /api/auth/login    | Login user     |
| GET    | /api/auth/profile  | Get profile    |
| PUT    | /api/auth/profile  | Update profile |

---

### 📦 Subscriptions

| Method | Endpoint               | Description             |
| ------ | ---------------------- | ----------------------- |
| GET    | /api/subscriptions     | Get all subscriptions   |
| POST   | /api/subscriptions     | Create subscription     |
| GET    | /api/subscriptions/:id | Get single subscription |
| PUT    | /api/subscriptions/:id | Update subscription     |
| DELETE | /api/subscriptions/:id | Delete subscription     |

---

### 💳 Payments

| Method | Endpoint            | Description    |
| ------ | ------------------- | -------------- |
| POST   | /api/payment/order  | Create order   |
| POST   | /api/payment/verify | Verify payment |

---

## 🔒 Environment Variables

| Variable            | Location | Description        |
| ------------------- | -------- | ------------------ |
| MONGO_URI           | Backend  | MongoDB connection |
| JWT_SECRET          | Backend  | JWT secret key     |
| RAZORPAY_KEY_ID     | Both     | Public key         |
| RAZORPAY_KEY_SECRET | Backend  | Secret key         |
| REACT_APP_API_URL   | Frontend | API base URL       |

---

## 👨‍💻 Developer

**Visali M**
Full Stack Developer (MERN)

---

## 📄 License

This project is developed for **educational purposes**.


