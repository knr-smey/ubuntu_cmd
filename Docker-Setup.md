# 🐳 Docker Setup Guide

A collection of Docker commands and Docker Compose templates for running databases, applications, and development environments.

## 📋 Table of Contents

* Docker Installation
* Docker Compose
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
* NestJS
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

## Check Version

```bash
docker --version
docker compose version
```

---

# 🐘 PostgreSQL

```bash
docker run -d \
  --name postgres17 \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=root \
  -e POSTGRES_DB=appdb \
  -p 5432:5432 \
  postgres:17
```

---

# 🔧 pgAdmin

```bash
docker run -d \
  --name pgadmin \
  -p 5050:80 \
  -e PGADMIN_DEFAULT_EMAIL=admin@example.com \
  -e PGADMIN_DEFAULT_PASSWORD=admin123 \
  dpage/pgadmin4
```

Access:

```text
http://localhost:5050
```

---

# 🐬 MySQL

```bash
docker run -d \
  --name mysql8 \
  -e MYSQL_ROOT_PASSWORD=root \
  -p 3306:3306 \
  mysql:8
```

---

# 🌐 phpMyAdmin

```bash
docker run -d \
  --name phpmyadmin \
  -e PMA_HOST=mysql8 \
  -p 8080:80 \
  phpmyadmin
```

---

# 🍃 MongoDB

```bash
docker run -d \
  --name mongodb \
  -p 27017:27017 \
  mongo:latest
```

---

# 🔍 Mongo Express

```bash
docker run -d \
  --name mongo-express \
  -e ME_CONFIG_MONGODB_SERVER=mongodb \
  -p 8081:8081 \
  mongo-express
```

---

# ⚡ Redis

```bash
docker run -d \
  --name redis \
  -p 6379:6379 \
  redis:latest
```

---

# 📊 Redis Insight

```bash
docker run -d \
  --name redisinsight \
  -p 5540:5540 \
  redis/redisinsight
```

---

# 🚀 Laravel

```bash
docker compose up -d
```

---

# 🟢 Node.js

```bash
docker run --rm node:22 node -v
```

---

# 🦀 Rust

```bash
docker run --rm rust:latest rustc --version
```

---

# 🌍 Nginx

```bash
docker run -d \
  --name nginx \
  -p 80:80 \
  nginx
```

---

# 🔧 Useful Commands

## List Containers

```bash
docker ps
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

## Remove Container

```bash
docker rm -f container_name
```

## Remove Unused Resources

```bash
docker system prune -a
```
