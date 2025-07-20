
# 🛠️ **Full Deployment Roadmap (Linux + Docker + AWS + CI/CD + Hosting)**

📆 **Duration:** 6 Weeks (1 session per 8 days)
🧭 **Goal:** Deploy a full-stack project using Dockerized architecture, AWS hosting, and GitHub CI/CD automation.

---

## 🔰 **Week 0 – Linux Basics (Self-Paced or Pre-Session)**

### 🔹 Topics:

* File System & Navigation: `cd`, `ls`, `pwd`, `mkdir`, `rm`, etc.
* Permissions & Ownership: `chmod`, `chown`, `sudo`
* Process Management: `ps`, `top`, `kill`, `systemctl`
* Networking: `curl`, `ping`, `netstat`, `ufw`, `ss`
* SSH & SCP: Connect & transfer to remote EC2
* Package Installation: `apt`, `git`, `node`, `docker`

📌 **Outcome**: Confidence in using Ubuntu-based AWS EC2 instance

---

## 🟩 **Week 1 – Docker Fundamentals + GitHub Repo Setup**

### 🔹 Topics:

* What is Docker? Why use it?
* Dockerfile, Docker Image, Docker Container
* `.dockerignore`, image optimization
* Build & run app in container: `docker build`, `docker run`
* Push image to DockerHub
* GitHub repo structure and best practices

📌 **Outcome**: App running in Docker locally + source code on GitHub

---

## 🟨 **Week 2 – Docker Compose + Local Database + ENV Handling**

### 🔹 Topics:

* Multi-container setup with `docker-compose.yml`
* Networking between frontend, backend, DB
* ENV variables via `.env` & Docker Compose
* Volumes for DB data persistence

📌 **Outcome**: Full stack app running locally in containers using `docker-compose`

---

## 🟦 **Week 3 – AWS & Web Hosting (Frontend)**

### 🔹 AWS Topics:

* AWS Free Tier account setup
* IAM Users, Access Keys, Permissions
* AWS S3:

  * Bucket creation
  * Static website hosting
  * Public access settings
  * Upload frontend build

### 🔹 Alternate Hosting:

* Netlify or GitHub Pages for quick deploy

📌 **Outcome**: React (or static frontend) hosted on S3, accessible via browser

---

## 🟥 **Week 4 – AWS EC2 Backend Deployment**

### 🔹 Topics:

* EC2 instance launch (Ubuntu)
* Key pair (`.pem`), SSH into EC2
* Install Docker, Git, Node.js
* Transfer project code using `scp` or `git clone`
* Run containers via `docker-compose`
* Open required ports in EC2 Security Group (3000, 5000, etc.)
* Optional: Elastic IP setup

📌 **Outcome**: Backend/API live and accessible on EC2 public IP

---

## 🟪 **Week 5 – CI/CD Automation with GitHub Actions**

### 🔹 Topics:

* What is CI/CD?
* GitHub Actions:

  * `.github/workflows/deploy.yml`
  * On push → build Docker image → SSH into EC2 → pull new image → restart
* Use GitHub Secrets to store private data (SSH key, IP, etc.)
* Optional: Notifications via email or Slack

📌 **Outcome**: On each push to main branch → auto deploy backend

---

## 🟫 **Week 6 – Final Polish + Monitoring + Demo**

### 🔹 Topics:

* View logs: `docker logs`, `journalctl`, `pm2 logs`
* Restart services: `docker-compose restart`
* S3 cache invalidation / frontend rebuild
* Optional:

  * Route 53 domain mapping
  * SSL using Let’s Encrypt + NGINX
  * CloudWatch setup for logs and monitoring

📌 **Outcome**: Production-ready app with full pipeline + basic observability

---

## 💡 **Mini Project: Daily Quotes App**

| Component   | Description                                     |
| ----------- | ----------------------------------------------- |
| Frontend    | React app that fetches & displays a daily quote |
| Backend     | Node.js + Express API with `/api/quote`         |
| Database    | MongoDB/Postgres to store quotes                |
| Admin Route | Secure route to add/edit/delete quotes          |

---

## 📁 **Suggested Project Structure**

```plaintext
daily-quotes-app/
├── backend/
│   ├── Dockerfile
│   └── src/
├── frontend/
│   ├── Dockerfile
│   └── public/
├── docker-compose.yml
├── .env
├── .github/
│   └── workflows/
│       └── deploy.yml
└── README.md
```

---

## 🔗 **Final Hosting Architecture**

```plaintext
[GitHub]
   ↓ (CI/CD - GitHub Actions)
[DockerHub] or [Image Built in EC2]
   ↓
[AWS EC2]
   - Backend via Docker
   - MongoDB in container
[AWS S3]
   - Frontend static files
[Route 53 / Domain] (Optional)
   ↓
Users access app on internet
```

---

## 📘 Optional Future Topics (After This Roadmap)

| Concept                      | Use                                    |
| ---------------------------- | -------------------------------------- |
| Kubernetes                   | Large-scale container orchestration    |
| ECS/Fargate                  | Serverless container deployment on AWS |
| Terraform                    | Infrastructure as Code                 |
| CloudWatch Logs              | Real-time monitoring                   |
| CI/CD with Jenkins or GitLab | Enterprise-level pipelines             |

---

## ✅ You Are Now Capable To:

* Dockerize and deploy full-stack apps
* Host static & dynamic content on AWS
* Automate code deployment via CI/CD
* Use Linux, GitHub, Docker, AWS together in a production setting

