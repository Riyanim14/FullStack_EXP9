🔐 Spring Boot Security Example (JWT Authentication)

A simple Spring Boot REST API project demonstrating User Registration, Login, and JWT-based Authentication using Spring Security.

🚀 Features
✅ User Registration (/register)
✅ User Login (/login)
✅ Password Encryption using BCrypt
✅ JWT Token Generation
✅ Secured API Endpoints
✅ Bearer Token Authorization
✅ Spring Security Integration
✅ RESTful API Design
🛠️ Tech Stack
Java (JDK 17+ / 21+)
Spring Boot
Spring Security
JWT (JSON Web Token)
Hibernate / JPA
MySQL (or any DB)
Maven
📂 Project Structure
src/
 ├── controller/
 ├── service/
 ├── repository/
 ├── entity/
 ├── config/
 ├── security/
 └── dto/
⚙️ Setup Instructions
1. Clone Repository
git clone https://github.com/your-username/spring-security-example.git
cd spring-security-example
2. Configure Database

Update application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/your_db
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
3. Run the Application
mvn spring-boot:run

App will start on:

http://localhost:8080
🔑 API Endpoints
📝 Register User

POST /register

{
  "id": 9,
  "username": "manjot",
  "password": "mj123"
}

✅ Response:

{
  "id": 9,
  "username": "manjot",
  "password": "<encrypted_password>"
}
🔐 Login User

POST /login

{
  "id": 9,
  "username": "manjot",
  "password": "mj123"
}

✅ Response:

<JWT_TOKEN>
🔒 Access Secured Endpoint

GET /students

Add Header:
Authorization: Bearer <JWT_TOKEN>

✅ Response:

[
  {
    "id": 1,
    "name": "Manjot",
    "marks": 89
  },
  {
    "id": 2,
    "name": "Harleen",
    "marks": 92
  }
]
🔄 Flow Diagram
User → Register → Stored in DB (Encrypted Password)

User → Login → JWT Token Generated

User → Access API → Sends JWT → Verified → Access Granted
🔐 Security Concepts Used
Authentication vs Authorization
Stateless Session using JWT
Password Hashing (BCrypt)
Filter-based JWT validation
Spring Security Configuration
🧪 Testing with Postman
Register a user
Login to get JWT token
Use token in Authorization tab
Access secured endpoints
📌 Future Improvements
Refresh Token implementation
Role-based Authorization (ADMIN/USER)
Swagger API Documentation
Exception Handling
Dockerization
👨‍💻 Author

Manjot Singh
B.Tech CSE (AIML)

⭐ Contribute
Feel free to fork this repo and improve it!

![WhatsApp Image 2026-03-31 at 22 18 49](https://github.com/user-attachments/assets/f4811dc8-0d60-4cc9-b139-aa50cee749b5)
![WhatsApp Image 2026-03-31 at 22 18 48](https://github.com/user-attachments/assets/16fe6027-f07b-4bd0-a40e-083afaa694d5)
![WhatsApp Image 2026-03-31 at 22 18 48 (2)](https://github.com/user-attachments/assets/491c53c6-3bdc-439e-ae24-a8c09c38f7f4)
![WhatsApp Image 2026-03-31 at 22 18 48 (1)](https://github.com/user-attachments/assets/10394939-94bc-467a-8995-40ea4cddbb75)
