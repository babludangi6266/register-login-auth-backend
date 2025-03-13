# Register-Login Authentication Backend

This is a **Node.js + Express + MongoDB** backend for a simple Register-Login System. It handles user registration, login, and basic user management efficiently and securely.

---

## 📁 Project Structure

```
register-login-auth-backend/
├── node_modules/          # Dependencies
├── config/
│    └── db.js             # MongoDB connection setup
├── models/
│    └── User.js           # User schema model
├── routes/
│    └── authRoutes.js     # Authentication routes
├── .env                   # Environment variables
├── .gitignore             # Ignore files
├── package.json           # Project metadata and scripts
└── server.js              # Main application entry point
```

---

## 🚀 Features

✅ **User Registration** (Name, Email, Phone, Password)<br>
✅ **User Login** (Email, Password)<br>
✅ **Password Hashing** (Using `bcryptjs`)<br>
✅ **JWT Token Generation** (For user authentication)<br>

---

## 🛠️ Technologies Used

- **Node.js**: JavaScript runtime environment.
- **Express.js**: Web framework for Node.js.
- **MongoDB**: NoSQL database for data storage.
- **Mongoose**: MongoDB object modeling for Node.js.
- **bcryptjs**: For securely hashing passwords.
- **jsonwebtoken (JWT)**: For generating access tokens.
- **dotenv**: For managing environment variables.

---

## 📌 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/register-login-auth.git
cd register-login-auth-backend
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Set Up Environment Variables
Create a `.env` file in the root directory and add the following:
```
MONGO_URI=mongodb://localhost:27017/registerlogin-auth
JWT_SECRET=your_secret_key
PORT=5000
```

### 4. Start the Server
```bash
npm run dev
```

---

## 📊 API Endpoints

### **1. Register a New User**
**Endpoint**: `POST /api/register`<br>
**Access**: Public

#### Request
```json
{
  "name": "Bablu Dangi",
  "email": "babludangi2000@gmail.com",
  "phone": "1234567890",
  "password": "12345"
}
```

#### Response
```json
{
  "message": "User registered successfully",
  "user": {
    "id": "user_id",
    "name": "Bablu Dangi",
    "email": "babludangi2000@gmail.com",
    "phone": "1234567890",
    "token": "your_jwt_token"
  }
}
```

---

### **2. User Login**
**Endpoint**: `POST /api/login`<br>
**Access**: Public

#### Request
```json
{
  "email": "babludangi2000@gmail.com",
  "password": "12345"
}
```

#### Response
```json
{
  "message": "Login successful",
  "user": {
    "id": "user_id",
    "name": "Bablu Dangi",
    "email": "babludangi2000@gmail.com",
    "phone": "1234567890",
    "token": "your_jwt_token"
  }
}

