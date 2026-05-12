# 🐋 DockerQuiz — Learn Docker by Playing

![Docker](https://img.shields.io/badge/Docker-Containerization-blue?logo=docker)
![Flask](https://img.shields.io/badge/Flask-Python-lightgrey?logo=flask)
![MongoDB](https://img.shields.io/badge/MongoDB-Database-green?logo=mongodb)
![Docker Compose](https://img.shields.io/badge/Docker%20Compose-MultiContainer-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

A hands-on, Kahoot-style quiz application built with **Python + Flask, MongoDB, and Mongo Express** — fully containerized using Docker Compose.

Built by **Samuel Nartey** as a beginner-friendly, zero-prerequisites introduction to Docker and container concepts.

---

# 📚 Overview

DockerQuiz is more than just a quiz application.

It is a practical Docker learning environment designed to help beginners understand:

- Multi-container applications
- Docker networking
- Service discovery
- Persistent volumes
- Container communication
- Docker Compose orchestration

Instead of reading isolated Docker commands, users interact with a real application stack running across multiple containers.

---

# 🚀 Quick Start

## Clone the Repository

```bash
git clone https://github.com/samuel-nartey/devops-labs.git
cd devops-labs
```

---

## Start All Containers

```bash
docker compose up --build
```

Docker will:

- Build the Flask application image
- Pull MongoDB image
- Pull Mongo Express image
- Create the internal Docker network
- Create persistent volumes
- Start all services

---

# 🌐 Application URLs

| Service | URL | Purpose |
|---|---|---|
| 🐋 Quiz Application | http://localhost:5000 | Play the Docker quiz |
| 🍃 Mongo Express | http://localhost:8081 | View MongoDB data visually |

---

# 📸 Screenshots

> Create a folder named `screenshots/` in your repository and place all screenshots there.

---

## 🏠 Quiz Homepage

_Add screenshot here_

```md
![Quiz Homepage](screenshots/homepage.png)
```

---

## ❓ Quiz Questions Interface

_Add screenshot here_

```md
![Question Interface](screenshots/question-page.png)
```

---

## ✅ Answer Feedback Page

_Add screenshot here_

```md
![Feedback Page](screenshots/feedback-page.png)
```

---

## 🏆 Final Results Page

_Add screenshot here_

```md
![Results Page](screenshots/results-page.png)
```

---

## 🍃 Mongo Express Dashboard

_Add screenshot here_

```md
![Mongo Express](screenshots/mongo-express.png)
```

---

## 🐳 Running Containers (`docker ps`)

_Add screenshot here_

```md
![Docker PS](screenshots/docker-ps.png)
```

---

## 🛠️ Docker Compose Startup Logs

_Add screenshot here_

```md
![Docker Compose Logs](screenshots/docker-compose-logs.png)
```

---

## 🌐 Docker Network Inspection

_Add screenshot here_

```md
![Docker Network](screenshots/docker-network.png)
```

---

# 🏗️ 3-Container Architecture

```text
┌────────────────────────────────────────────────────────────┐
│                     quiz-network (bridge)                 │
│                                                            │
│  ┌──────────────┐     ┌──────────────┐    ┌─────────────┐ │
│  │  quiz-app    │────▶│    mongo     │◀──▶│mongo-express│ │
│  │ Flask :5000  │     │ Mongo :27017 │    │   :8081     │ │
│  └──────────────┘     └──────────────┘    └─────────────┘ │
└────────────────────────────────────────────────────────────┘
```

---

# 🧠 Key Docker Concept — Container DNS

The Flask application connects to MongoDB using the Docker Compose service name:

```python
MONGO_URI = "mongodb://mongo:27017/"
```

Docker automatically resolves `mongo` to the correct container IP using Docker’s built-in DNS system.

This is how real-world containerized applications communicate internally.

---

# 🛠️ Technologies Used

- Docker
- Docker Compose
- Python 3
- Flask
- MongoDB
- Mongo Express
- Jinja2
- PyMongo

---

# 📂 Project Structure

```bash
running docker compose/
│
├── app.py
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── .dockerignore
├── README.md
│
└── templates/
    ├── base.html
    ├── index.html
    ├── question.html
    ├── feedback.html
    └── results.html
```

---

# ⚙️ Docker Compose Configuration

The application stack contains three services:

## quiz-app
- Flask web application
- Built from custom Dockerfile
- Runs on port 5000

## mongo
- MongoDB database
- Stores quiz profiles and results
- Uses persistent Docker volumes

## mongo-express
- Web-based MongoDB admin dashboard
- Accessible on port 8081

---

# 💾 MongoDB Collections

The application stores data in:

| Collection | Purpose |
|---|---|
| `profiles` | User profile information |
| `quiz_states` | Live quiz progress |
| `results` | Final quiz scores |

---

# ▶️ Useful Docker Commands

## View Running Containers

```bash
docker ps
```

---

## View Application Logs

```bash
docker logs dockerquiz-app -f
```

---

## Open Shell Inside Flask Container

```bash
docker exec -it dockerquiz-app bash
```

---

## Open MongoDB Shell

```bash
docker exec -it dockerquiz-mongo mongosh
```

---

## Inspect Docker Networks

```bash
docker network inspect quiz-network
```

---

## Stop Containers

```bash
docker compose down
```

---

## Remove Containers and Volumes

```bash
docker compose down -v
```

---

# 🎯 Learning Outcomes

Through this project, I gained practical experience with:

- Docker containerization
- Docker Compose orchestration
- Multi-container applications
- Docker networking
- Persistent storage using volumes
- MongoDB integration
- Flask containerization
- Service discovery using Docker DNS
- Real-world application architecture

---

# 🔥 Future Improvements

Potential enhancements include:

- User authentication
- Leaderboards
- Kubernetes deployment
- CI/CD automation with GitHub Actions
- Redis caching
- Multi-stage Docker builds
- Container vulnerability scanning
- Docker image publishing to Docker Hub

---

# 🤝 Contributing

Contributions and suggestions are welcome.

To contribute:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a pull request

---

# 👨‍💻 Author

**Samuel Nartey**

- GitHub: https://github.com/samuel-nartey
- Repository: https://github.com/samuel-nartey/devops-labs

---

# ⭐ Support

If this project helped you learn Docker or containerization, consider giving the repository a star.

---

# 📜 License

MIT License — free to use, modify, and share.
