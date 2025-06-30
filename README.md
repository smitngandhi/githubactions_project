# Flask CI-CD Project

This is a simple Flask application integrated with GitHub Actions for CI/CD and Docker deployment.

## 🛠 Project Structure

```
.
├── app.py                 # Main Flask app
├── requirements.txt       # Python dependencies
├── test_app.py            # Unit tests using pytest
├── DockerFile             # Dockerfile to containerize the app
├── .gitignore             # Files and folders to ignore in Git
└── .github/
    └── workflows/
        └── cicd.yml       # GitHub Actions workflow file
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the app locally

```bash
python app.py
```

### 4. Run tests

```bash
pytest test_app.py
```

## 🐳 Docker Usage

### Run the Docker container

```bash
docker pull smit1025/flask-app
docker run -p 5000:5000 flask-app
```

## ⚙️ GitHub Actions

Whenever you push to the `main` branch or create a pull request, the GitHub Actions workflow (`cicd.yml`) will:

* Install dependencies
* Run tests
* Build and push a Docker image to DockerHub (on main push)

## 🔐 Secrets Required (in GitHub repo settings)

* `DOCKER_USERNAME`
* `DOCKER_PASSWORD`