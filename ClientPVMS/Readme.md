# 🌐 PVMS Frontend – Passport Visa Management System

The **PVMS Frontend** is a web-based user interface built using **JSP (Java Server Pages)**, served directly through the Spring Boot MVC backend. It allows users to interact with the core functionalities of the PVMS platform, including registration, authentication, passport/visa services, and admin approvals, using dynamically rendered JSP views.

---

## 🎯 Goal

Deliver an accessible, role-based user experience for applicants (passport/visa) and administrators, rendered via Spring Boot's embedded MVC view engine.

---

## 🧩 Controllers

The frontend module also defines MVC controllers to serve views and handle form submissions. These interact with REST APIs exposed by the backend to manage passport and visa operations.

### Main Controllers:

* `AdminController`: Loads admin dashboard and fetches user applications.
* `LoginController`: Authenticates users and redirects to dashboards.
* `UserRegistrationController`: Handles new user registration forms.
* `PassportApplyController`: Sends passport application data to backend.
* `VisaApplyController`: Manages visa form submission.
* `VisaCancelController`: Initiates visa cancellation requests.

---

## 🧰 Technologies Used

* **JSP + JSTL** (Java view rendering)
* **HTML/CSS** (via JSPs)
* **Bootstrap 4** (for layout & styling)
* **Spring Boot MVC** (view resolver and controllers)
* **Java 17+**

---

## 📁 Core Pages

### 1. 📝 Registration Page

* Form for new applicants
* Auto-populates user type (passport/visa)
* Submission handled via Spring controller

### 2. 🔐 Login Page

* User ID and Password input
* Authenticates and redirects based on role (user/admin)

### 3. 🧑‍💼 User Dashboard

* Shows application options

  * Apply Passport
  * Apply Visa
  * Reissue Passport
  * Cancel Visa
* Displays status of previous submissions

### 4. 📋 Admin Dashboard

* View all applications
* Approve/reject passport and visa requests
* Generate reports (PDF-style summaries)

### 5. 📄 Dynamic JSPs

* Conditional rendering based on login role and session flags
* Feedback messages using Bootstrap alerts

---

## 🗂️ Folder Structure

```
src/
└── main/
    └── webapp/
        └── WEB-INF/
            └── views/
                ├── login.jsp
                ├── register.jsp
                ├── dashboard.jsp
                ├── applyPassport.jsp
                ├── applyVisa.jsp
                ├── reissue.jsp
                ├── cancelVisa.jsp
                └── adminPanel.jsp
```

---

## 🧪 How to View Frontend

### Prerequisites:

* Backend must be running (Spring Boot)

### Access Pages:

* Home: `http://localhost:8080/PassportManagementSystem`
* Register: `/register.jsp`
* Login: `/login.jsp`
* Dashboard: `/dashboard.jsp` (after login)

---

## 🎨 Styling

* Responsive layout via **Bootstrap 4**
* Minimal inline CSS – mostly class-based
* Form validation using standard HTML5 attributes

---

## ⚙️ View Resolver Setup

Defined in `application.properties`:

```properties
spring.mvc.view.prefix=/WEB-INF/views/
spring.mvc.view.suffix=.jsp
```

---

## 💡 Notes

* All views are served by the **backend service**
* There is no standalone React/Angular SPA – rendering is handled server-side
* Ideal for beginners learning **Spring Boot + JSP** stack

---

## 👨‍💻 Author

**Hanuma Ramavath**
Java | JSP | Spring Boot | MVC Web UI Developer
🔗 GitHub: [@netfreaker-ally](https://github.com/netfreaker-ally)

---


