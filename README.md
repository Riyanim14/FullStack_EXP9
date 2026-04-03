# 🔐 JWT Authentication using Spring Boot

This project demonstrates a basic implementation of **JWT (JSON Web Token) authentication** using Spring Boot.

---

## 🚀 Features

* User login with username & password
* JWT token generation
* Protected API endpoint
* Token-based authentication using headers
* Spring Security integration

---

## 🛠️ Tech Stack

* Java
* Spring Boot
* Spring Security
* JWT (io.jsonwebtoken)
* Maven

---

## 📁 Project Structure

```
src/main/java/com/AML_3A/JWTAuth/
│
├── controller/
│   └── AuthController.java
│
├── security/
│   ├── JwtUtil.java
│   └── JwtFilter.java
│
├── config/
│   └── SecurityConfig.java
│
└── JwtAuthApplication.java
```

---

## 🔑 API Endpoints

### 1️⃣ Login (Generate Token)

**POST**

```
http://localhost:8080/api/login
```

**Body (x-www-form-urlencoded):**

```
username=admin
password=123
```

**Response:**

```
JWT Token (example)
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

---

### 2️⃣ Access Protected API

**GET**

```
http://localhost:8080/api/secure
```

**Headers:**

```
Authorization: Bearer YOUR_TOKEN
```

**Response:**

```
You accessed protected API!
```

---

## ⚙️ How It Works

1. User sends login request with credentials
2. Server validates credentials
3. JWT token is generated using `JwtUtil`
4. Client sends token in Authorization header
5. `JwtFilter` intercepts request and validates token
6. If valid → access granted
7. If invalid/missing → access denied

---

## 🔐 JWT Flow

```
Client → Login → Server → Generate Token
Client ← Token ← Server

Client → Request (with token) → Server
Server → Validate Token → Allow/Deny
```

---

## ⚠️ Notes

* This is a basic implementation for learning purposes
* Credentials are hardcoded (not secure for production)
* No database integration
* Token validation is minimal

---

## 🚀 Future Improvements

* Add MySQL database
* Implement UserDetailsService
* Use BCrypt password hashing
* Role-based authentication (Admin/User)
* Refresh tokens
* Exception handling & logging

---

## ▶️ How to Run

1. Clone the repository

```
git clone https://github.com/your-username/jwt-auth-project.git
```

2. Open in Eclipse / IntelliJ / VS Code

3. Run the application

```
JwtAuthApplication.java
```

4. Server runs at:

```
http://localhost:8080
```

---

## 🧪 Testing

Use Postman:

1. Call `/api/login` → get token
2. Use token in header → call `/api/secure`

---

## 👨‍💻 Author

**Riyan Imtiyaz**

---

## ⭐ If you found this helpful

Give this repo a ⭐ on GitHub!
