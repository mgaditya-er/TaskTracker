# TaskTracker Backend

TaskTracker is a production-ready backend API built with FastAPI for managing users and tasks, featuring automated testing, containerization, and CI/CD.

---

## Tech Stack

* FastAPI
* PostgreSQL
* SQLAlchemy
* Alembic
* Pytest & pytest-cov
* Docker & Docker Compose
* GitHub Actions

---

## Features

### Users

* Create and retrieve users
* Email uniqueness validation

### Tasks

* Create, retrieve, update, and delete tasks
* Filter tasks by owner and status
* Input and ownership validation

### Health Endpoints

* `/healthz`
* `/readyz`

---

## DevOps Highlights

* Multi-stage Docker image running as a non-root user
* Docker Compose setup with PostgreSQL health checks
* Automated testing and coverage reporting via GitHub Actions
* Automatic Docker Hub image publishing after successful CI

---

## Project Structure

```text
app/
├── api/
├── core/
├── db/
├── middleware/
├── models/
├── schemas/
└── services/

tests/
docs/
.github/workflows/
```
