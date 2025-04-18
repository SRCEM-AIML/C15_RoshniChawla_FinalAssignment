# Flask + Django Web Apps with Docker Compose

This project demonstrates how to build and run two web applications — one using Flask and the other using Django — containerized using Docker and managed with Docker Compose.

---

## Project Overview

This repository contains:

- A Flask application with a simple homepage and input form.
- A Django application with:
  - Item listing view
  - Admin panel
  - Form to add new items
- Individual Dockerfiles for each application.
- A Docker Compose configuration to run both apps together.

---

## Directory Structure

```
C15_RoshniChawla_FinalAssignment/
├── flask_app/
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── django_app/
│   ├── manage.py
│   ├── mysite/
│   ├── itemlist/
│   ├── requirements.txt
│   └── Dockerfile
│
├── docker-compose.yml
└── README.md
```

---

## How to Run the Project

### Prerequisites

- Docker
- Docker Compose

### Steps

1. Open a terminal in the project directory.
2. Run the following command:

```
docker-compose up --build
```

3. Access the apps in your browser:
   - Flask App: http://localhost:5000
   - Django App: http://localhost:8000

---

## Flask Application

- A simple Python Flask app.
- Renders a homepage with a form to collect name and age.
- Displays a personalized greeting.
- Runs on port 5000.
- Uses its own Dockerfile for containerization.

---

## Django Application

- A Django project with an app called `itemlist`.
- Features:
  - Homepage displaying a list of items
  - Form to add new items
  - Admin panel for managing items
- Uses SQLite as the database.
- Runs on port 8000.
- Dockerized with a separate Dockerfile.

---

## Docker Hub Images

You can pull the pre-built images directly from Docker Hub:

- Flask App:
  ```
  docker pull roshnichawla/flask-app
  ```
  https://hub.docker.com/r/roshnichawla/flask-app

- Django App:
  ```
  docker pull roshnichawla/django-app
  ```
  https://hub.docker.com/r/roshnichawla/django-app

---

## Django Admin

To apply migrations:

```
docker exec -it final-django-app python manage.py migrate
```

To create a superuser:

```
docker exec -it final-django-app python manage.py createsuperuser
```

Admin Panel is available at:  
http://localhost:8000/admin

---

## Author

Roshni Chawla  
GitHub: https://github.com/RoshniChawla25  
Docker Hub: https://hub.docker.com/u/roshnichawla
