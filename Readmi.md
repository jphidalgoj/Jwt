Spring Boot: JWT Authentication Project
This project demonstrates how to implement a JWT Authentication functionality in an Spring Boot application.

Overview
This project showcases the implementation of a JWT Authentication feature in an Spring Boot application.

Technologies used:

Spring Boot 3
Spring Security 6
jsonwebtoken


Installation
Follow these steps to install and run the project:

Clone the repository: git clone https://github.com/irojascorsico/spring-boot-jwt-authenticadion.git
Navigate to the project directory: cd your-repo
Build the project using Maven:: mvn clean install
Run the project: mvn spring-boot:run
Test the API Rest using Postman or another application at http://localhost:8080.




Ejemplo de Escenario de Prueba
1. Login
   o Request:
   json
   Copiar código
   POST /api/auth/login
   {
   "username": "admin",
   "password": "password123"
   }
   o Response:
   json
   Copiar código
   {
   "token": "Bearer <jwt-token>"
   }
2. Endpoint Público
   o Request: GET /api/public
   o Response: "Endpoint público: No requiere autenticación"
3. Endpoint Protegido (Sin Token)
   o Request: GET /api/protected
   o Response: 401 Unauthorized
4. Endpoint Protegido (Con Token)
   o Request: GET /api/protected con encabezado:
   makefile
   Copiar código
   Authorization: Bearer <jwt-token>
   o Response: "Endpoint protegido: Usuario autenticado como admin"