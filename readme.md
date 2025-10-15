# 🧠 QR Code Generator – Dockerized Application

### 📌 Overview
This project is a **Dockerized Python application** that creates QR codes for any given URL.  
It shows how to use Docker, GitHub Actions, and Python together for automation and secure deployment.


## My DockerHub Image

![Docker QR Image](qr_codes/QRCode_20251015010558.png "My QR Code Link")

## My Github Repository

![Github Repo](qr_codes/QRCode_20251015013400.png "My QR Code Link")

---

### ⚙️ Features
- Creates QR codes from custom URLs.
- Saves files automatically in the `qr_codes/` folder.
- Uses a small and secure base image (`python:3.12-slim-bullseye`).
- Runs with a non-root user for better security.
- Automatically builds and uploads the image to DockerHub using GitHub Actions.

---

### 🧰 Tools Used
- **Python 3.12**
- **qrcode**, **Pillow**
- **Docker** for containerization
- **GitHub Actions** for automation
- **DockerHub** for storing images

---

### 🚀 How to Run

#### Clone the Repository
```bash
git clone https://github.com/arhamidrees63/assignment7.git
cd assignment7

Install Requirements
pip install -r requirements.txt

Run the App Locally
python main.py --url "https://www.njit.edu"


This will create a QR image inside the qr_codes/ folder.

🐳 Run with Docker
Build the Docker Image
docker build -t qr_codemaker .

Run the Container
docker run --rm -v $(pwd)/qr_codes:/app/qr_codes qr_codemaker --url "https://www.njit.edu"

🔄 GitHub Actions Workflow

When code is pushed to the main branch:

The Docker image is built and tested.

The image is uploaded to DockerHub automatically.

👉 View DockerHub Repository

💭 Reflection

This project helped me understand how Docker makes it easy to build and deploy applications.
I learned how to write a Dockerfile, use GitHub Actions for automation, and securely push images to DockerHub quite a new and challening module
Now I feel more confident about using Docker and automation in real projects