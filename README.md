# 🐋 DockerQuiz — Learn Docker by Playing

![Docker](https://img.shields.io/badge/Docker-Containerization-blue?logo=docker)
![Flask](https://img.shields.io/badge/Flask-Python-lightgrey?logo=flask)
![MongoDB](https://img.shields.io/badge/MongoDB-Database-green?logo=mongodb)
![Docker Compose](https://img.shields.io/badge/Docker%20Compose-MultiContainer-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

A hands-on, Kahoot-style quiz application built with **Python + Flask, MongoDB, and Mongo Express** — fully containerized using Docker Compose.

Built as a beginner-friendly introduction to Docker, container networking, volumes, and multi-container applications.

---

# 📚 Overview

DockerQuiz is designed to help beginners learn Docker by interacting with a real multi-container application instead of isolated examples.

The project demonstrates:

- Multi-container applications
- Docker Compose orchestration
- Container networking
- Docker DNS/service discovery
- Persistent volumes
- Flask + MongoDB integration
- Real-world container architecture

---

# 🚀 Features

✅ Flask-based quiz application  
✅ MongoDB database integration  
✅ Mongo Express database dashboard  
✅ Multi-container Docker Compose stack  
✅ Persistent Docker volumes  
✅ Docker networking and DNS  
✅ Interactive quiz with scoring system  
✅ Beginner-friendly architecture  

---

# 🏗️ Architecture

```text
┌────────────────────────────────────────────────────────────┐
│                    quiz-network (bridge)                  │
│                                                            │
│  ┌──────────────┐     ┌──────────────┐    ┌─────────────┐ │
│  │  quiz-app    │────▶│    mongo     │◀──▶│mongo-express│ │
│  │ Flask :5000  │     │ Mongo :27017 │    │   :8081     │ │
│  └──────────────┘     └──────────────┘    └─────────────┘ │
└────────────────────────────────────────────────────────────┘
```

---

# 📸 Screenshots

> Create a folder named `screenshots/` in your repository and place all screenshots there.

---

## 🏠 Homepage

![Homepage](screenshots/homepage.png)

---

## ❓ Quiz Questions

![Questions](screenshots/questions.png)

---

## ✅ Feedback Page

![Feedback](screenshots/feedback.png)

---

## 🏆 Final Results

![Results](screenshots/results.png)

---

## 🍃 Mongo Express Dashboard

![Mongo Express](screenshots/mongo-express.png)

---

## 🐳 Running Containers

![Docker PS](screenshots/docker-ps.png)

---

## 🌐 Docker Network

![Docker Network](screenshots/docker-network.png)

---

## 🛠️ Docker Compose Logs

![Compose Logs](screenshots/docker-compose-logs.png)

---

# 🛠️ Technologies Used

- Docker
- Docker Compose
- Python
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

# ⚙️ Setup Instructions

## Clone Repository

```bash
git clone https://github.com/samuel-nartey/devops-labs.git
cd devops-labs
```

---

## Start the Application

```bash
docker compose up --build
```

---

# 🌐 Access the Application

| Service | URL |
|---|---|
| Quiz Application | http://localhost:5000 |
| Mongo Express | http://localhost:8081 |

---

# ▶️ Useful Docker Commands

## View Running Containers

```bash
docker ps
```

---

## View Logs

```bash
docker logs dockerquiz-app -f
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

# 💾 MongoDB Collections

| Collection | Purpose |
|---|---|
| profiles | User profile information |
| quiz_states | Current quiz progress |
| results | Final quiz results |

---

# 🎯 Learning Outcomes

Through this project, I gained hands-on experience with:

- Docker containerization
- Docker Compose orchestration
- Container networking
- Docker DNS and service discovery
- Persistent storage using Docker volumes
- Flask application containerization
- MongoDB integration
- Real-world multi-container architecture

---

# 🔥 Future Improvements

Potential enhancements include:

- Kubernetes deployment
- GitHub Actions CI/CD
- Redis caching
- User authentication
- Leaderboards
- Multi-stage Docker builds
- Container vulnerability scanning

---

# 👨‍💻 Author

**Samuel Nartey**

- GitHub: https://github.com/samuel-nartey
- Repository: https://github.com/samuel-nartey/devops-labs

---

# ⭐ Support

If this project helped you learn Docker, consider giving the repository a star.

---

# 📜 License

MIT License — free to use, modify, and share.
