# Notes for Personal Referencing

## Dockerfile

- `FROM python:3.13-slim-bookworm` pulls the base image of a python's official specific version from Docker Hub.
- `ENV PYTHONDONTWRITEBYTECODE 1` prevents Python from writing pyc files to disc.
- `ENV PYTHONUNBUFFERED 1` prevents Python from buffering stdout and stderr.
- `WORKDIR /app` sets the working directory to /app.
- `COPY requirements.txt .` copies the requirements.txt file to current directory.
- `RUN pip install --upgrade pip` upgrades pip to the latest version.
- `RUN pip install -r requirements.txt` installs the dependencies in the requirements.txt file.
- `COPY . .` copies the current directory contents to the container at /app.
- `CMD ["python", "app.py"]` specifies the command to run on container start-up.
- `EXPOSE 8000` exposes port 8000 to the host machine.
- `CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]` runs the Django development server on container start-up.
---
## Docker Image Setup

Run these commands in the terminal to build and run the Docker image.

- `docker build .` builds an image from the Dockerfile in the current directory.
- `docker build -t docker-image .` builds an image with the tag docker-image in the current directory.
- `docker images` lists all the images on the host machine.
- 