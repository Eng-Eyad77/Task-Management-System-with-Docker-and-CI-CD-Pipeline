
# ✅ Task-Management-System


---

## 📌 Project Overview

This project is a web-based **Spring Boot MVC** application for managing tasks. It allows users to perform full **CRUD** operations on tasks, including setting their priority and status. The project integrates **JUnit testing**, **Jenkins CI/CD pipelines**, and **Docker containerization** for efficient deployment.

---

## 🧩 Features

- Create, update, and delete tasks.
- Set task status and priority (Low, Medium, High).
- View all tasks in a task list view.
- MVC structure using Spring Boot.
- Fully tested using **JUnit**.
- Jenkins pipeline for CI/CD automation.
- Packaged and deployed using **Docker**.

---

## 🛠️ Technology Stack

- **Backend:** Java 17, Spring Boot
- **Frontend:** Thymeleaf (HTML views)
- **Build Tool:** Maven
- **Testing:** JUnit
- **CI/CD:** Jenkins
- **Containerization:** Docker

---

## 📂 Core Components

- **Model:** `Task` class representing the entity.
- **Repository:** `TaskRepository` and `TaskRepositoryInterface` using Spring Data JPA.
- **Service:** `TaskService` for business logic.
- **Controller:** `TaskController` handling user interactions.
- **Views:** HTML pages for task creation, editing, setting priority, and listing.

---

## 🧪 Testing Strategy

- **Unit Testing:** Validates each method (getters/setters, CRUD operations).
- **Integration Testing:** Confirms components interact as expected.
- **RTM (Requirement Traceability Matrix):** Maps each requirement to its corresponding test cases.
- **Automation:** All tests are integrated into Jenkins pipeline and run automatically.

---

## 🧬 Example Test Cases

| Test Case ID | Scenario | Input | Expected Output | Status |
|--------------|----------|--------|------------------|--------|
| TC-01 | Test getter/setter for `id` | id = 1 | 1 | ✅ Pass |
| TC-06 | Set task priority | High | High | ✅ Pass |
| TC-10 | Delete task by ID | id = 1 | Task deleted | ✅ Pass |

---

## 🔁 Jenkins Pipeline Stages

1. **Checkout** – Clone from GitHub repository  
2. **Build** – Compile the project with Maven  
3. **Test** – Run JUnit test cases  
4. **Package** – Generate `.jar` file  
5. **Docker Build** – Create Docker image  
6. **Deployment** – Deploy app to port `8081` using Docker

---

## 🐳 Docker Deployment Commands

```bash
docker stop myapp || true
docker rm myapp || true
docker run -d --name myapp -p 8081:8080 myapp:latest
```

---

## 📌 Application Requirements

| Req ID | Description |
|--------|-------------|
| REQ-01 | Task model with: id, title, description, status, priority |
| REQ-02 | View list of tasks |
| REQ-03 | Create new tasks |
| REQ-04 | Edit tasks |
| REQ-05 | Delete tasks |
| REQ-06 | Set task priority (Low, Medium, High) |

---

## 📦 Packaging

- Packaged into `.jar` via Maven.
- Dockerized with a two-stage Dockerfile (build + runtime).
- Port `8081` exposed and mapped in container.

---

## 👥 Team Members

- Eyad Adnan Maccawy
- Enad Abdulmohsen Alharbi
- Turki Abdullah Alotaibi
- Jawad Khaled Alotaibi
