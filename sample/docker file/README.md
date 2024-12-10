# Python Docker Setup

This repository contains a Dockerfile to set up and run a Python application in a Docker container.

## Dockerfile Overview

This Dockerfile creates a minimal and efficient environment to run a Python application using the official `python:3.9-slim` image.

### Dockerfile Instructions

1. **Base Image**  
   ```dockerfile
   FROM python:3.9-slim
   ```
   This uses the lightweight, official Python 3.9 image as the base, optimized for minimal size and resource usage.

2. **Working Directory**  
   ```dockerfile
   WORKDIR /app
   ```
   Sets `/app` as the working directory in the container, where all application files will reside and be executed.

3. **Copy Application Files**  
   ```dockerfile
   COPY . /app
   ```
   Copies all files from the current directory on the host machine to the `/app` directory in the container.

4. **Install Dependencies**  
   ```dockerfile
   RUN pip install --no-cache-dir -r requirements.txt
   ```
   Installs the dependencies listed in `requirements.txt` using `pip`, with `--no-cache-dir` to prevent caching, reducing the image size.

5. **Expose Port**  
   ```dockerfile
   EXPOSE 8080
   ```
   Exposes port 8080 in the container, allowing the application to be accessed externally on this port.

6. **Run the Application**  
   ```dockerfile
   CMD ["python", "app.py"]
   ```
   Specifies the default command to start the application by running `app.py` with Python.

### Instructions to Build and Run

1. **Build the Docker Image**
   ```bash
   docker build -t my-python-app .
   ```

2. **Run the Container**
   ```bash
   docker run -p 8080:8080 my-python-app
   ```
