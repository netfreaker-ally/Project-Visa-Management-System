# 🛂 Passport Visa Management System (PVMS)

The **Passport Visa Management System (PVMS)** is a full-stack, role-based web application that allows users to apply for passports and visas, while administrators manage and approve those applications. Built entirely in Java using **Spring Boot MVC** for the backend and **JSP** for the frontend, PVMS showcases a classic 3-tier web architecture ideal for learning and understanding full-stack Java development.

---

## 📦 Project Structure

```
pvms/
├── pvms-backend/       # Spring Boot backend (MVC, Services, JPA)
├── pvms-frontend/      # JSP pages and static assets
└── README.md           # (This file)
```

---

## 🎯 Project Highlights

* Complete registration and login module with role-based dashboards
* Auto-generated IDs and passwords for users (e.g., `VISA-1234`, `PASS-4567`)
* Passport & Visa application workflows with database persistence
* Dynamic JSP rendering and session-based access control
* Admin approval flow for passport/visa applications
* Responsive UI using Bootstrap
* Embedded H2 Database with option to switch to MySQL

---

## 🧰 Technologies Used

| Layer         | Tech Stack                           |
| ------------- | ------------------------------------ |
| Frontend      | JSP, JSTL, HTML5, CSS3, Bootstrap 4  |
| Backend       | Spring Boot MVC, Spring Data JPA     |
| Database      | H2 (In-memory), MySQL (optional)     |
| View Resolver | Internal Spring Boot + JSP templates |
| Build Tool    | Maven                                |
| Java Version  | Java 17                              |

---

## 🗂️ Backend Features (`pvms-backend/`)

* Spring Boot project with controller → service → repository layers
* DTOs and model-driven logic
* Password and ID generation logic
* Passport expiry calculated (10 years)
* Visa fee and expiry calculated based on destination and occupation
* Refunds handled during visa cancellation
* Controllers for:

  * Registration
  * Login
  * Passport apply / reissue
  * Visa apply / cancel

🧠 Refer: [`pvms-backend/README.md`](./pvms-backend/README.md)

---

## 🌐 Frontend Features (`pvms-frontend/`)

* JSP-based form rendering and session-based navigation
* Conditional dashboards for user/admin roles
* Alert messages and feedback based on action outcomes
* Controllers serve JSP views and redirect to logic in backend

🧠 Refer: [`pvms-frontend/README.md`](./pvms-frontend/README.md)

---

## ⚙️ Setup & Run Instructions

### ✅ Prerequisites:

* JDK 17+
* Maven
* (Optional) MySQL if not using H2

### 🔽 Steps:

```bash
git clone https://github.com/netfreaker-ally/pvms.git
cd pvms
```

#### Run Backend:

```bash
cd pvms-backend
mvn spring-boot:run
```

#### Access:

* App: `http://localhost:8080/PassportManagementSystem`
* H2 Console: `http://localhost:8080/h2-console`

> All JSPs are served by the backend – there’s no separate frontend server.

---

## 📚 Learning Outcomes

✅ Full-stack MVC using Spring Boot and JSP
✅ Entity-to-DTO mappings and controller flow
✅ Session and role-based navigation logic
✅ Understanding database persistence with H2/MySQL
✅ Classic monolith app split into layered responsibilities

---

## 👨‍💻 Author

**Hanuma Ramavath**
Java | Spring Boot | Full-Stack Developer | MVC Projects
🔗 GitHub: [@netfreaker-ally](https://github.com/netfreaker-ally)

---

## 📘 Additional Notes

* Ideal for academic submission or entry-level job demo
* Could be further enhanced by adding JWT security, REST-based frontend, or converting to microservices
