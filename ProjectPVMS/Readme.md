# 🛂 PVMS Backend – Passport Visa Management System

This is the backend module of the **Passport Visa Management System (PVMS)**, a Spring Boot project developed using classic **Spring MVC** architecture. It focuses on building a working CRUD-based backend using JSP pages, servlets/controllers, service layers, and JDBC/JPA-backed persistence. This project was designed with learning goals in mind, ideal for mastering foundational Spring Boot concepts.

---

## 🔧 Tech Stack

* **Spring Boot** (MVC + Web)
* **Spring Data JPA** (Hibernate)
* **H2** (In-memory DB) / **MySQL** (optional)
* **JSP** and JSTL (View layer)
* **Tomcat** embedded server (via Spring Boot)

---

## 📁 Modules Implemented

### 1. 👥 User Registration

* Users can register as either **passport** or **visa** applicants.
* User ID is auto-generated based on application type (e.g., `PASS-1234`, `VISA-4567`).
* Password is system-generated using a custom format.
* Citizen type is determined based on DOB (Infant, Teen, Adult, etc.).

### 2. 🔐 Login Authentication

* Validates user credentials (User ID + Password).
* Redirects users to appropriate dashboards based on role.

### 3. 📄 Apply Passport

* Requires address, state, city, country, PIN, service type, and booklet type.
* Generates **Passport ID** and calculates expiry date (+10 years).
* Stores passport data in the database.

### 4. 🌍 Apply Visa

* User selects destination, occupation, and application date.
* Visa ID and expiry are generated based on occupation.
* Fee is calculated based on destination + occupation.

### 5. ♻️ Passport Re-Issue

* Re-applies passport with updated reason and details.
* Retains old records and creates new issue + expiry.

### 6. ❌ Visa Cancellation

* Calculates refund/cancellation cost based on visa age and user category.
* Updates status to cancelled.

---

## 🗂️ Project Structure

```
PVMS/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/pvms/
│   │   │       ├── controller
│   │   │       ├── service
│   │   │       ├── repository
│   │   │       ├── model/entity
│   │   │       └── utils
│   │   └── resources/
│   │       ├── application.properties
│   │       └── static + templates (JSP)
└── pom.xml
```

---

## 💡 How to Run

### ✅ Prerequisites:

* JDK 17+
* Maven

### 🔽 Steps:

```bash
git clone https://github.com/netfreaker-ally/pvms-backend.git
cd pvms-backend
mvn clean install
mvn spring-boot:run
```

### 🌐 Access:

* App URL: `http://localhost:8080/PassportManagementSystem`
* H2 Console: `http://localhost:8080/h2-console`

---

## ⚙️ Sample Configuration (`application.properties`)

```properties
spring.datasource.url=jdbc:h2:mem:pvmsdb
spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.mvc.view.prefix=/WEB-INF/views/
spring.mvc.view.suffix=.jsp
```

---

## 📊 Example Use Cases

* **Register** → `UserController.register()`
* **Login** → `LoginController.authenticate()`
* **Apply Passport** → `PassportController.apply()`
* **Apply Visa** → `VisaController.submit()`
* **Reissue Passport** → `ReIssueController.process()`
* **Cancel Visa** → `VisaCancellationController.cancel()`

---

## 📌 Learning Highlights

✅ JSP + Spring Boot integration
✅ Simple MVC layering: Controller → Service → Repository
✅ Entity design and persistence logic
✅ Application.properties & embedded DB usage
✅ Custom ID and password generation logic

---

## 👨‍💻 Author

**Hanuma Ramavath**
Spring Boot Developer | Java Enthusiast | Learning-Oriented Projects
🔗 GitHub: [@netfreaker-ally](https://github.com/netfreaker-ally)

---
