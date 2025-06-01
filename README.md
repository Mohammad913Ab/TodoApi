# 📝 ToDo API

A simple and secure task management API built with Django and Django REST Framework.  
This project allows users to register, log in via JWT authentication, and manage their personal to-do tasks through a clean, well-structured API.

---

## 🚀 Features

- ✅ User registration & JWT-based login
- 📌 CRUD operations for personal tasks
- 🔐 Authenticated access per user
- 📄 Auto-generated API documentation via Swagger/OpenAPI
- 🧼 Clean code structure with Django best practices

---

## ⚙️ Tech Stack

- Python 3.11+
- Django 5.2
- Django REST Framework
- Simple JWT (`rest_framework_simplejwt`)
- drf-spectacular (for schema & docs)

---

## 📁 Installation

1. **Clone the repository:**

```bash
git clone https://github.com/your-username/todo-api.git
cd todo-api
```

2. **Create virtual environment:**

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies:**

```bash
pip install -r requirements.txt
```

4. **Run migrations:**

```bash
python manage.py migrate
```

5. **Start the server:**

```bash
python manage.py runserver
```

---

## 🔐 Authentication

This API uses **JWT tokens** for authentication.

- Get token:
  ```
  POST /api/token/
  ```

- Refresh token:
  ```
  POST /api/token/refresh/
  ```

- Include the token in requests:
  ```
  Authorization: Bearer <your_token>
  ```

---

## 📚 API Documentation

Once the server is running, you can access the auto-generated docs:

- **Schema (OpenAPI JSON):**
  ```
  /api/schema/
  ```

- **Swagger UI:**
  ```
  /api/docs/swagger/
  ```

---

## ✅ Endpoints Overview

| Method | Endpoint              | Description             |
|--------|-----------------------|-------------------------|
| POST   | /api/register/        | User registration       |
| POST   | /api/token/           | Get JWT access token    |
| GET    | /api/tasks/           | List tasks              |
| POST   | /api/tasks/           | Create a task           |
| GET    | /api/tasks/{id}/      | Retrieve a task         |
| PUT    | /api/tasks/{id}/      | Update a task           |
| DELETE | /api/tasks/{id}/      | Delete a task           |
