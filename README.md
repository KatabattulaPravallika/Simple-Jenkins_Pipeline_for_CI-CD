# GitHub Actions CI/CD Demo

## 🔧 What It Does
- Builds and tests a Flask app using GitHub Actions
- Uses Docker to containerize the app
- Runs curl to verify the app runs properly inside the container

## 🚀 How to Use

1. Push this project to GitHub
2. On every push to `main`, the pipeline:
   - Builds Docker image
   - Runs the app
   - Tests the app using `curl`

Check progress under: **GitHub → Actions tab**

## 🐳 Local Docker Test
```bash
docker build -t my-app-image .
docker run -p 5000:5000 my-app-image
