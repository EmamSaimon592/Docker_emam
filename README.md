<p align="center">
  <img src="/images/dockerpic.png" alt="Cover Image" width="100%" />
</p>

#  Docker Guide

This README provides a complete reference for Docker usage including basic commands, Dockerfile examples, Docker Compose setup, and tips.

---

## What is Docker?

Docker is a platform for developing, shipping, and running applications inside containers.

---

##  Installation

- [Install Docker](https://docs.docker.com/get-docker/)
- Run `docker --version` to check installation

---

## Basic Docker Commands

### Images

```bash
docker pull ubuntu                # Download image
docker images                    # List local images
docker rmi image_name            # Remove image

docker run -it ubuntu bash       # Run Ubuntu container interactively
docker run -d nginx              # Run container in detached mode
docker ps                        # List running containers
docker ps -a                     # List all containers
docker stop container_id         # Stop a container
docker rm container_id           # Remove a container

```

### Docker Compose

```bash
docker-compose up --build         # Build and start containers
docker-compose down               # Stop and remove containers
```

## Author

**Imam Hossain**
International Islamic University Chittagong (IIUC)
[LinkedIn](https://linkedin.com/in/your-profile) | [GitHub](https://github.com/your-username)

## docker-compose.yml

```yaml
version: '3.8'

services:
  app:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/app
    environment:
      - ENV=development
```

---

