# Docker-Setup.md

# 🐳 Docker Setup Guide

A collection of Docker commands and Docker Compose templates for running databases, applications, and development environments.

## 📋 Table of Contents

* Docker Installation
* Docker Network
* PostgreSQL
* pgAdmin
* MySQL
* phpMyAdmin
* MongoDB
* Mongo Express
* Redis
* Redis Insight
* Laravel
* Node.js
* Rust
* Nginx
* Useful Commands

---

# 🐳 Docker Installation

## Install Docker

```bash
sudo apt update
sudo apt install docker.io -y
```

## Start Docker

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

## Check Docker

```bash
docker --version
docker ps
```

---

# 🌐 Docker Network

## Create Custom Network

```bash
docker network create pg-network
```

## List Networks

```bash
docker network ls
```

## Inspect Network

```bash
docker network inspect pg-network
```

---

# 🐘 PostgreSQL

## Run PostgreSQL

```bash
docker run -d \
  --name postgres \
  --network pg-network \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=root \
  -e POSTGRES_DB=appdb \
  -p 5432:5432 \
  postgres:17
```

## Connect PostgreSQL Shell

```bash
docker exec -it postgres psql -U postgres
```

## Stop PostgreSQL

```bash
docker stop postgres
```

## Remove PostgreSQL

```bash
docker rm -f postgres
```

---

# 🔧 pgAdmin

## Run pgAdmin

```bash
docker run -d \
  --name pgadmin \
  --network pg-network \
  -e PGADMIN_DEFAULT_EMAIL=admin@example.com \
  -e PGADMIN_DEFAULT_PASSWORD=admin123 \
  -p 5050:80 \
  dpage/pgadmin4
```

## Access pgAdmin

```text
http://localhost:5050
```

### Login

```text
Email: admin@example.com
Password: admin123
```

### Add PostgreSQL Server

```text
Name: Local PostgreSQL

Host: postgres
Port: 5432
Database: postgres
Username: postgres
Password: root
```

---

# 🐬 MySQL

## Run MySQL

```bash
docker run -d \
  --name mysql8 \
  -e MYSQL_ROOT_PASSWORD=root \
  -p 3306:3306 \
  mysql:8
```

## Connect MySQL

```bash
docker exec -it mysql8 mysql -u root -p
```

---

# 🌐 phpMyAdmin

## Run phpMyAdmin

```bash
docker run -d \
  --name phpmyadmin \
  -e PMA_HOST=mysql8 \
  -p 8080:80 \
  phpmyadmin
```

## Access phpMyAdmin

```text
http://localhost:8080
```

---

# 🍃 MongoDB

## Run MongoDB

```bash
docker run -d \
  --name mongodb \
  -p 27017:27017 \
  mongo:latest
```

---

# 🔍 Mongo Express

## Run Mongo Express

```bash
docker run -d \
  --name mongo-express \
  -e ME_CONFIG_MONGODB_SERVER=mongodb \
  -p 8081:8081 \
  mongo-express
```

## Access Mongo Express

```text
http://localhost:8081
```

---

# ⚡ Redis

## Run Redis

```bash
docker run -d \
  --name redis \
  -p 6379:6379 \
  redis:latest
```

---

# 📊 Redis Insight

## Run Redis Insight

```bash
docker run -d \
  --name redisinsight \
  -p 5540:5540 \
  redis/redisinsight
```

## Access Redis Insight

```text
http://localhost:5540
```

---

# 🚀 Laravel

## Start Laravel Containers

```bash
docker compose up -d
```

## Stop Laravel Containers

```bash
docker compose down
```

---

# 🟢 Node.js

## Check Node.js Version

```bash
docker run --rm node:22 node -v
```

## Open Node.js Container

```bash
docker run -it --rm node:22 bash
```

---

# 🦀 Rust

## Check Rust Version

```bash
docker run --rm rust:latest rustc --version
```

## Open Rust Container

```bash
docker run -it --rm rust:latest bash
```

---

# 🌍 Nginx

## Run Nginx

```bash
docker run -d \
  --name nginx \
  -p 80:80 \
  nginx
```

---

# 🔧 Useful Docker Commands

## List Running Containers

```bash
docker ps
```

## List All Containers

```bash
docker ps -a
```

## List Images

```bash
docker images
```

## View Logs

```bash
docker logs container_name
```

## Enter Container

```bash
docker exec -it container_name bash
```

## Stop Container

```bash
docker stop container_name
```

## Start Container

```bash
docker start container_name
```

## Restart Container

```bash
docker restart container_name
```

## Remove Container

```bash
docker rm -f container_name
```

## Remove Image

```bash
docker rmi image_name
```

## Remove Unused Resources

```bash
docker system prune -a
```

## Remove Unused Volumes

```bash
docker volume prune
```

## Remove Unused Networks

```bash
docker network prune
```

---

## 👨‍💻 Author

**KNR-Smey**
