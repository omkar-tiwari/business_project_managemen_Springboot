# Business Management System — Spring Boot

A full-stack Business Management Web Application built with **Spring Boot**, **Thymeleaf**, and **MySQL** — featuring customer management, inventory tracking, order processing, and role-based admin/user access control.

---

## Features

- **Customer Management** — Add, update, and delete customer information
- **Inventory Management** — Track products, stock levels, and pricing
- **Order Management** — Create and manage customer orders
- **User Authentication** — Secure login for admin and staff members
- **Role-Based Access Control** — Separate admin and user panels
- **Thymeleaf Templates** — Dynamic server-side HTML rendering
- **Database Integration** — MySQL with Spring Data JPA

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Spring Boot 3.x |
| Frontend | Thymeleaf, HTML, CSS |
| Database | MySQL 8 |
| ORM | Spring Data JPA / Hibernate |
| Build Tool | Maven |
| Java Version | Java 21 |

---

## Getting Started

### Prerequisites

- JDK 21+
- MySQL 8.0+
- Maven (or use the included `mvnw` wrapper)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/omkar-tiwari/business_project_managemen_Springboot.git
   cd business_project_managemen_Springboot
   ```

2. **Create the MySQL database**
   ```sql
   CREATE DATABASE businessproject;
   ```

3. **Configure database credentials** in `src/main/resources/application.properties`
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/businessproject
   spring.datasource.username=root
   spring.datasource.password=your_password
   spring.jpa.hibernate.ddl-auto=update
   server.port=2330
   ```

4. **Run the application**
   ```bash
   ./mvnw spring-boot:run
   ```

5. **Open in browser**
   ```
   http://localhost:2330/home
   ```

6. **Add an admin** manually in the database to log in:
   ```sql
   INSERT INTO admin (admin_name, admin_email, admin_password, admin_number)
   VALUES ('Admin', 'admin@business.com', '1234', '9876543210');
   ```

---

## Default Login Credentials

| Role | Email | Password |
|------|-------|----------|
| Admin | admin@business.com | 1234 |
| User | (register via admin panel) | — |

---

## Project Structure

```
src/
├── main/
│   ├── java/com/business/
│   │   ├── controllers/       # MVC Controllers
│   │   ├── entities/          # JPA Entities (Admin, User, Product, Orders)
│   │   ├── repositories/      # Spring Data Repositories
│   │   ├── services/          # Business Logic
│   │   └── loginCredentials/  # Login DTO classes
│   └── resources/
│       ├── templates/         # Thymeleaf HTML templates
│       └── application.properties
```

---

## License

This project is open source and available under the [MIT License](LICENSE).
