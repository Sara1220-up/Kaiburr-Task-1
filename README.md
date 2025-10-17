

```markdown
# 🧩 Task 1 — Spring Boot REST API with MongoDB Integration

This project implements a **Spring Boot REST API** that performs CRUD operations on tasks using **MongoDB** as the backend database.  
It demonstrates how to connect a Spring Boot application to MongoDB, expose REST endpoints, and validate data flow through API testing.

---

## ⚙️ Objective

1. Develop a RESTful web service using **Spring Boot**.  
2. Integrate the service with **MongoDB**.  
3. Perform CRUD operations on tasks (Create, Read, Update, Delete).  
4. Validate API responses using **Postman / cURL** and confirm data persistence in MongoDB.

---

## 🧰 Technologies Used

| Component | Purpose |
|------------|----------|
| **Java 17** | Programming language |
| **Spring Boot 3** | Framework for REST API development |
| **Spring Web** | REST API endpoint exposure |
| **Spring Data MongoDB** | Database integration layer |
| **MongoDB** | NoSQL database for storage |
| **Maven** | Build automation and dependency management |
| **Postman / cURL** | API testing tools |

---

## 📁 Project Structure

```

Kaiburr-Task-1/
│
├── pom.xml
├── src/
│   ├── main/
│   │   ├── java/com/kaiburr/taskmanager/
│   │   │   ├── controller/TaskController.java
│   │   │   ├── model/Task.java
│   │   │   ├── repository/TaskRepository.java
│   │   │   └── service/TaskService.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/
│       └── java/com/kaiburr/taskmanager/
├── task_1_screenshots/
└── README.md

````

---

## ⚙️ Configuration

### MongoDB Setup

1. Install and start MongoDB:
   ```bash
   net start MongoDB
   mongosh
   use kaiburrdb
````

2. Update your `application.properties`:

   ```properties
   spring.data.mongodb.database=kaiburrdb
   spring.data.mongodb.port=27017
   spring.data.mongodb.host=localhost
   server.port=8080
   ```

---

## 🧩 REST Endpoints

| HTTP Method | Endpoint      | Description             |
| ----------- | ------------- | ----------------------- |
| `PUT`       | `/tasks`      | Create or update a task |
| `GET`       | `/tasks`      | Retrieve all tasks      |
| `GET`       | `/tasks/{id}` | Retrieve a task by ID   |
| `DELETE`    | `/tasks/{id}` | Delete a task by ID     |

---

## 🧠 Example cURL Commands

```bash
# Create or Update a Task
curl -X PUT http://localhost:8080/tasks \
  -H "Content-Type: application/json" \
  -d '{"id":"1","name":"Print Hello","owner":"Sarayu","command":"echo Hello Kaiburr"}'

# Retrieve All Tasks
curl http://localhost:8080/tasks

# Execute Task
curl -X PUT http://localhost:8080/tasks/1/execute

# Delete a Task
curl -X DELETE http://localhost:8080/tasks/1
```

---

## 🧾 Verification & Results

### ⚙️ Spring Boot Installation

![Spring Boot Installation](./task_1_screenshots/springboot_insatallation.png)

### 🧠 Backend Simulation

![Backend Simulation](./task_1_screenshots/Backend_simulation.png)

### 🧩 Connected to MongoDB

![Connected to MongoDB](./task_1_screenshots/connected%20to%20mongodb.png)

### 💾 Task Stored in Database

![Stored in Database](./task_1_screenshots/stored%20in%20database.png)

### 🧪 API Testing with Postman / cURL

![Tasks API Testing](./task_1_screenshots/tasks_api_testing.png)

### 🗂️ Project Files View

![Files Structure](./task_1_screenshots/files.png)

---

## 🚀 How to Run the Application

1. Clone the repository:

   ```bash
   git clone https://github.com/Sara1220-up/Kaiburr-Task-1.git
   cd Kaiburr-Task-1
   ```

2. Build and run the application:

   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

3. Verify the API at:
   👉 [http://localhost:8080/tasks](http://localhost:8080/tasks)

---

## 🧩 Outcome

✅ Successfully built and deployed a Spring Boot REST API integrated with MongoDB.
✅ Verified data persistence between API and MongoDB.
✅ CRUD operations validated via cURL and Postman.

---

## 👩‍💻 Author

**Sarayu Mandadi**
📦 Kaiburr Internship — Task 1 Submission
📧 GitHub: [Sara1220-up](https://github.com/Sara1220-up)

```

   net start MongoDB
mongosh
show dbs
use kaiburrdb
