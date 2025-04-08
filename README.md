# 🚀 Simple Jenkins Pipeline for CI/CD

This project demonstrates a basic CI/CD pipeline using **Jenkins** and **Docker** to automate the build and deployment process for a simple Python Flask application.

---

## 📌 Objective

- Set up a basic Jenkins pipeline
- Automate the build, test, and deploy stages using Docker
- Trigger the pipeline automatically on code changes

---

## 🧱 Project Structure

```
.
├── app.py            # Flask application
├── Dockerfile        # Container configuration
└── Jenkinsfile       # CI/CD pipeline script
```

---

## ⚙️ Technologies Used

- Jenkins (Self-hosted or Cloud)
- Docker
- GitHub (as source control)
- Python & Flask

---

## 📦 Jenkinsfile Overview

The pipeline includes the following stages:

1. **Clone** – Pull the latest code from the GitHub repo  
2. **Build** – Build a Docker image of the app  
3. **Test** – (Placeholder) Run automated tests  
4. **Deploy** – Run the app container

```groovy
pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/KatabattulaPravallika/Simple-Jenkins_Pipeline_for_CI-CD.git'
            }
        }

        stage('Build') {
            steps {
                script {
                    docker.build('jenkins-pipeline-app')
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests... (placeholder)'
            }
        }

        stage('Deploy') {
            steps {
                script {
                    docker.image('jenkins-pipeline-app').run('-d -p 5000:5000')
                }
            }
        }
    }
}
```

---

## 🚀 Running the App Locally

```bash
# Build the Docker image
docker build -t jenkins-pipeline-app .

# Run the container
docker run -p 5000:5000 jenkins-pipeline-app
```

Then open your browser at: http://localhost:5000

---

## 🔁 CI/CD Flow

> On each code push:
- Jenkins fetches the latest code
- Builds and runs the Docker container
- Verifies the app runs correctly

---


## 📚 Learning Outcome

- Understood how Jenkins automates CI/CD workflows
- Learned Docker-based deployment in Jenkins
- Created and configured a Jenkins pipeline from scratch

---

## 📬 Author

**Katabattula srilakshminarasimha pravallika**  
🔗 https://github.com/KatabattulaPravallika

---

