# Django Notes App with Docker

A modern notes application built with Django, React, and Docker.

## 🚀 Quick Start

1. Clone the repository:
```bash
git clone https://github.com/avinash0123/note-app.git
cd note-app
```

2. Create environment file:
```bash
cp .env.example .env  # Edit .env with your settings if needed
```

3. Start the application:
```bash
docker-compose up --build
```

4. Access the application:
- Frontend: http://localhost
- Backend API: http://localhost:8000

## 🛠️ Tech Stack
- Backend: Django, Django REST Framework
- Frontend: React.js
- Database: MySQL
- Web Server: Nginx
- Containerization: Docker, Docker Compose

## 📦 Docker Services
- `django_app`: Django backend service
- `db`: MySQL database
- `nginx`: Reverse proxy and static file server

## 🔧 Environment Variables
Create a `.env` file with:
```
DB_NAME=test_db
DB_USER=root
DB_PASSWORD=root
DB_PORT=3306
DB_HOST=db_cont
```

## 📝 Notes
- The application uses Docker Compose for orchestration
- Data is persisted in the `./data/mysql/db` directory
- Nginx serves as a reverse proxy on port 80
