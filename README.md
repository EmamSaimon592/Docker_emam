<p align="center">
  <img src="images/dockergif.gif" alt="Emam Saimon Docker" width="600" height="300">
</p>


#  🐳 what is Docker?
Docker is an open-source platform that enables developers to automate application deployment, scaling, and management using containerization. Containers are lightweight, portable, and self-sufficient environments that include everything an application needs to run, such as code, libraries, dependencies, and runtime.

#  🐳 Why Docker?
Containerization – Packages applications and dependencies into standardized containers.
Portability – Containers run consistently across different environments (e.g., development, testing, production).
Efficiency – Uses fewer resources than virtual machines (VMs) since containers share the host OS kernel.
Isolation – Each container runs independently, preventing conflicts between applications.
Scalability – Easily scale applications up or down using Docker Swarm or Kubernetes.
Core Components of Docker:
Docker Engine – The core component that runs and manages containers.
Docker Hub – A cloud-based repository for sharing container images.
Docker Compose – A tool to define and run multi-container applications.
Docker file – A script defining how to build a Docker image.
![image](https://github.com/user-attachments/assets/7e4cb1a9-522c-4577-bb5f-c941ae978f05)

# 🐳 Docker Commands Cheat Sheet

A quick reference for commonly used Docker commands for **images**, **containers**, **volumes**, and **networks**.

---

## 📦 IMAGES

### 📋 List All Local Images
```bash
docker images
```

### 🗑️ Delete an Image
```bash
docker rmi <image_name>
```

### 🧹 Remove Unused Images (Dangling Only)
```bash
docker image prune
```

### 🧹 Remove All Unused Images
```bash
docker image prune -a
```

### 🏗️ Build an Image from Dockerfile
```bash
docker build -t <image_name>:<version> .
```

### 🔄 Build Without Cache
```bash
docker build -t <image_name>:<version> . --no-cache
```

---

## 📦 CONTAINERS

### 📋 List Running Containers
```bash
docker ps
```

### 📋 List All Containers (including stopped)
```bash
docker ps -a
```

### 🚀 Run a Container
```bash
docker run -it <image_name>
```

### 🚀 Run and Map Ports
```bash
docker run -d -p <host_port>:<container_port> <image_name>
```

### ⏹️ Stop a Running Container
```bash
docker stop <container_id>
```

### ❌ Remove a Container
```bash
docker rm <container_id>
```

---

## 🗃️ VOLUMES

### 📋 List Volumes
```bash
docker volume ls
```

### ➕ Create a Volume
```bash
docker volume create <volume_name>
```

### 🗑️ Remove a Volume
```bash
docker volume rm <volume_name>
```

### 🧹 Prune Unused Volumes
```bash
docker volume prune
```

---

## 🌐 NETWORKS

### 📋 List Networks
```bash
docker network ls
```

### ➕ Create a Network
```bash
docker network create <network_name>
```

### ❌ Remove a Network
```bash
docker network rm <network_name>
```

### 📎 Connect a Container to a Network
```bash
docker network connect <network_name> <container_name>
```

### 🔌 Disconnect a Container from a Network
```bash
docker network disconnect <network_name> <container_name>
```

---

## 🧼 Clean Up Everything (Use With Caution!)
```bash
docker system prune -a
```

Removes:
- All stopped containers  
- All networks not used by at least one container  
- All dangling images and build cache  
- All unused volumes (with `--volumes` flag)

---

## ✅ Helpful Tips

- `<image_name>` can be an image ID or name (`ubuntu`, `nginx`, etc.).
- `<container_id>` is usually the first few characters of `docker ps -a` output.
- Use `docker logs <container_id>` to debug container output.

---

Feel free to fork or star this repo if you find it useful!

<p align="center">
  <img src="images/dockerpic.png" alt="Emam saimon docker">
</p>








