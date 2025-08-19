
# 🎓 Student Management System

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/RohanBansal01/Student_Management_System?style=social)](https://github.com/RohanBansal01/Student_Management_System/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/RohanBansal01/Student_Management_System?style=social)](https://github.com/RohanBansal01/Student_Management_System/network/members)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)]()

A **Java-based Student Management System** built using **JDBC + MySQL**.  
This project follows a layered architecture (Controller → Service → DAO → Database) to perform CRUD operations on student records.  

---

## ✨ Features
- Add new student records  
- View all students  
- Search student by ID  
- Update student details  
- Delete student records  
- Validations for data integrity (email, phone, age, etc.)  
- CLI (Command-Line Interface) menu-driven application  

---

## 🛠️ Tech Stack
- **Language**: Java (JDK 21)  
- **Database**: MySQL  
- **JDBC**: MySQL Connector/J  
- **IDE**: Eclipse  

---

## 📂 Project Structure
```

student\_management\_system/
│── src/
│   ├── com.studentmanagement.controller/
│   │   └── StudentController.java
│   ├── com.studentmanagement.dao/
│   │   └── StudentDao.java
│   ├── com.studentmanagement.database/
│   │   ├── StudentDatabase.java
│   │   └── config.properties
│   ├── com.studentmanagement.model/
│   │   └── Student.java
│   ├── com.studentmanagement.service/
│   │   └── StudentService.java
│   └── module-info.java
│
└── Referenced Libraries/

````

---

## ⚙️ Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/RohanBansal01/Student_Management_System.git
cd Student_Management_System
````

### 2. Configure MySQL Database

* Create a database named `studentdb`
* Run the following SQL:

```sql
CREATE TABLE students (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  age INT NOT NULL,
  email VARCHAR(100) UNIQUE NOT NULL,
  course VARCHAR(50) NOT NULL,
  phone VARCHAR(10) NOT NULL
);
```

### 3. Update `config.properties`

```
db.url=jdbc:mysql://localhost:3306/studentdb
user=root
password=root
```

### 4. Add MySQL JDBC Driver

Download **MySQL Connector/J** and add it to your project’s classpath.

### 5. Run the Application

```bash
javac -d bin src/com/studentmanagement/**/*.java
java com.studentmanagement.controller.StudentController
```

---

## 🚀 Usage

* Choose from menu options:

  1. Add Student
  2. View All Students
  3. Search Student by ID
  4. Update Student
  5. Delete Student
  6. Exit

---

## 🤝 Contribution

Contributions are welcome!

1. **Fork** the repository
2. **Create** a new branch:

   ```bash
   git checkout -b feature-name
   ```
3. **Commit** your changes:

   ```bash
   git commit -m "Added new feature"
   ```
4. **Push** to your branch:

   ```bash
   git push origin feature-name
   ```
5. Open a **Pull Request**

---

## 👨‍💻 Author

* **Rohan Bansal**
  [GitHub](https://github.com/RohanBansal01)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---
