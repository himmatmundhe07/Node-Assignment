# 🎓 Student Management API

A simple REST API built using **Node.js**, **Express**, and **CORS** to manage student data.

This API provides endpoints to:
- Get all students
- Find the topper
- Calculate average CGPA
- Count total students
- Get student by ID
- Filter students by branch

---

## 🚀 Tech Stack

- Node.js
- Express.js
- CORS

---

## 📦 Installation

1. Clone the repository

```bash
git clone <your-repo-link>
```

2. Navigate to the project folder

```bash
cd <project-folder>
```

3. Install dependencies

```bash
npm install
```

4. Install required packages (if not already installed)

```bash
npm install express cors
```

5. Start the server

```bash
node index.js
```

Server will start at:

```
http://localhost:3000
```

---

## 📚 Student Data Structure

Each student object contains:

```json
{
  "id": Number,
  "name": String,
  "branch": String,
  "semester": Number,
  "cgpa": Number
}
```

---

## 🔗 API Endpoints

### 1️⃣ Get All Students

```
GET /students
```

Returns list of all students.

---

### 2️⃣ Get Topper (Highest CGPA)

```
GET /students/topper
```

Returns student(s) with highest CGPA.

If no students found → `404`

---

### 3️⃣ Get Average CGPA

```
GET /students/average
```

Returns:

```json
{
  "AverageCgpa": number
}
```

If no data found → `404`

---

### 4️⃣ Get Total Student Count

```
GET /students/count
```

Returns:

```json
{
  "totalStudents": number
}
```

---

### 5️⃣ Get Student by ID

```
GET /students/:id
```

Example:

```
GET /students/1
```

If student not found → `404`

---

### 6️⃣ Get Students by Branch

```
GET /students/branch/:branchName
```

Example:

```
GET /students/branch/CSE
```

Branch filtering is **case-insensitive**.

If no students found → `404`

---

## ⚙️ Server Configuration

- Runs on **Port 3000**
- CORS enabled for cross-origin requests

---

## 📌 Example Base URL

```
http://localhost:3000
```

Example:

```
http://localhost:3000/students
```

---

## 🛠 Future Improvements

- Add POST route to create students
- Add PUT route to update students
- Add DELETE route
- Connect to a database (MongoDB / MySQL)
- Add input validation
- Add error handling middleware

---

## 📄 License

This project is for learning purposes.
