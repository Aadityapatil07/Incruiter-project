# Authentication API

This is a **Node.js & Express** authentication API that allows users to **register, login, and change passwords**. The app uses **MongoDB** as a database and includes authentication via **JWT (JSON Web Tokens)**.

## 🚀 Features
- User Registration
- User Login
- Password Change
- Secure Authentication with JWT
- Password Hashing with bcrypt
- Cookie-based Authentication

## 🛠️ Tech Stack
- **Backend:** Node.js, Express.js
- **Database:** MongoDB with Mongoose
- **Security:** JWT, bcrypt, cookie-parser
- **CORS Support:** Enabled for frontend integration

## 🔧 Installation & Setup

### 1️⃣ Clone the Repository
```sh
git clone https://github.com/Aadityapatil07/Incruiter-project.git
cd Incruiter-project
```

### 2️⃣ Install Dependencies
```sh
npm install
```

### 3️⃣ Set Up Environment Variables
Create a `.env` file in the root directory and add the following:
```env
PORT=8000
CORS_ORIGIN=*
ACCESS_TOKEN_SECRET=mYq2xZ9pLn8tJf4Kg5wR3dV7B6aHYQXpVcN7TyLqMw9FkJ2BnR8P6X4VdYWpNzJ3
ACCESS_TOKEN_EXPIRY=1d
REFRESH_TOKEN_SECRET=aV4dK87xJq3L9tRfNzB2wPn5yH6gVcYmQXpLkR9vTyHwM3BnZ8FpJ6LqX2dR7YwN
REFRESH_TOKEN_EXPIRY=10d

MONGODB_URI=mongodb+srv://Adityapatil:Aditya24@cluster0.1nrty.mongodb.net/Incruiter

```

### 4️⃣ Start the Server
```sh
npm run dev  # If using nodemon
```
The API will run on `http://localhost:8000`

---

## 📌 API Endpoints

### **1️⃣ User Registration**
**Endpoint:** `POST /api/v1/users/register`
```json
{
  "fullName": "John Doe",
  "email": "johndoe@example.com",
  "password": "SecurePass123"
}
```

### **2️⃣ User Login**
**Endpoint:** `POST /api/v1/users/login`
```json
{
  "email": "johndoe@example.com",
  "password": "SecurePass123"
}
```

### **3️⃣ Change Password**
**Endpoint:** `POST /api/v1/users/change-password`
```json
{
  "oldPassword": "SecurePass123",
  "newPassword": "NewSecurePass456"
}
```