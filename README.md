

````markdown
# 🧩 Kaiburr Task 1 – Java Backend and REST API Example

---

## 🎯 Objective
Implement a **Java Spring Boot application** that provides a REST API for managing "Task" objects.  
Each Task represents a shell command that can be run, stored, and queried from a MongoDB database.

---

## ⚙️ Tech Stack
- **Language:** Java 17  
- **Framework:** Spring Boot  
- **Database:** MongoDB  
- **Tools:** Postman / cURL for API testing  

---

## 📁 Project Features

### Endpoints Implemented
| HTTP Method | Endpoint | Description |
|--------------|-----------|-------------|
| **GET** | `/tasks` | Fetch all tasks or a single task by ID |
| **PUT** | `/tasks` | Create or update a task |
| **DELETE** | `/tasks/{id}` | Delete a task by ID |
| **GET** | `/tasks/find?name={name}` | Search tasks by partial name |
| **PUT** | `/tasks/{id}/execution` | Execute a shell command and store results |

---

## 🧠 Data Model

### Task Object
```json
{
  "id": "123",
  "name": "Print Hello",
  "owner": "Shiva Prasad",
  "command": "echo Hello World",
  "taskExecutions": [
    {
      "startTime": "2025-01-15T10:00:00Z",
      "endTime": "2025-01-15T10:00:02Z",
      "output": "Hello World"
    }
  ]
}
````

---

## 🗃️ MongoDB Configuration

* Application connects to MongoDB using connection details defined in `application.properties`.
* Each created task is stored as a document inside MongoDB.

---
## 📷 Screenshots Overview

| Step | Screenshot |
|---|---|
| 1️⃣ Spring Boot Installation | ![Spring Boot Installation](./task%201_scrrenshots/springboot_insatallation.png) |
| 2️⃣ MongoDB Connection Established | ![MongoDB Connection](./task%201_scrrenshots/connected%20to%20mongodb.png) |
| 3️⃣ Backend Simulation (Application Running) | ![Backend Simulation](./task%201_scrrenshots/Backend_simulation.png) |
| 4️⃣ API Testing via Postman | ![API Testing](./task%201_scrrenshots/tasks_api_testing.png.png) |
| 5️⃣ Data Stored in MongoDB | ![Data Stored in Database](./task%201_scrrenshots/stored%20in%20database.png) |
| 6️⃣ Files Overview in Project | ![Files Overview](./task%201_scrrenshots/files.png) |

---

## ✅ Execution Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/Kaiburr-Task-1.git
   ```
2. Navigate to the project:

   ```bash
   cd Kaiburr-Task-1
   ```
3. Build and run the app:

   ```bash
   mvn spring-boot:run
   ```
4. Verify the API:

   * Open [http://localhost:8080/tasks](http://localhost:8080/tasks)
   * Test endpoints using Postman or cURL.

---

## 📊 Output Verification

* The API successfully creates, fetches, deletes, and executes tasks.
* MongoDB stores each task and its execution history.
* All requests return expected HTTP responses (200, 201, 404, etc.).

---

## ✅ Conclusion

Task 1 successfully demonstrates:

* Building REST APIs using Spring Boot
* Integration with MongoDB
* Command execution and persistence

---

🧩 Author
👤 Sarayu Mandadi
📦 Kaiburr Internship – Task 1 Submission
