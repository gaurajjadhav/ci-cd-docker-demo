# 🚀 CI/CD Pipeline with GitHub Actions & Docker

This project demonstrates a simple yet powerful CI/CD pipeline using **GitHub Actions** and **Docker**. It automatically builds and pushes a Docker image of a Flask web application to Docker Hub whenever code is pushed to the main branch.

---

## 📌 Project Structure

ci-cd-docker-demo/

├── app.py # Flask web application

├── Dockerfile # Docker image configuration

├── requirements.txt # Python dependencies

└── .github/

└── workflows/

└── docker-ci.yml # GitHub Actions CI/CD workflow

---

## 🛠️ Tech Stack & Tools Used

- **Python (Flask)** – Web framework
- **Docker** – Containerization platform
- **GitHub** – Version control and source repository
- **GitHub Actions** – Automation and CI/CD pipeline
- **Docker Hub** – Image registry to host Docker images

---

## ⚙️ Workflow Steps

1. User pushes code to the GitHub `main` branch.
2. GitHub Actions:
   - Checks out the code
   - Logs into Docker Hub using stored secrets
   - Builds a Docker image
   - Pushes the image to Docker Hub
3. Docker image is available publicly at:  
   🔗 [https://hub.docker.com/r/gauraj/ci-cd-docker-demo](https://hub.docker.com/r/gauraj/ci-cd-docker-demo)

---

## 📄 Setup Instructions

### 🔧 Clone the Repository
```bash
git clone https://github.com/gaurajjadhav/ci-cd-docker-demo.git
cd ci-cd-docker-demo
```

### Build & Run the Docker Image Locally
```bash
docker build -t gauraj/ci-cd-docker-demo .
docker run -p 5000:5000 gauraj/ci-cd-docker-demo
```

Visit `http://localhost:5000` to view the app.

---

### GitHub Actions Secrets Configuration
Added the following repository secrets in GitHub:

DOCKER_USERNAME → Docker Hub username

DOCKER_PASSWORD → Docker Hub access token

---

### Result
Every code push to main automatically:

- Builds the Flask app as a Docker image.

- Pushes it to Docker Hub.

- Makes the latest version available for deployment.

  ---

### Author
### Gauraj Jadhav
**DevOps & Cloud Enthusiast**
**Linkedin : 'https://www.linkedin.com/in/gaurajjadhav'**
