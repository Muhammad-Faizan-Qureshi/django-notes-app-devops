# Django Notes App — DevOps Project

A notes application built with React and Django, containerized with Docker Compose, using MySQL and Nginx as a reverse proxy. Deployed on AWS EC2 as part of a hands-on DevOps learning journey.

## Technologies

- Django and Django REST Framework
- React
- Docker and Docker Compose
- MySQL
- Nginx
- AWS EC2

## Requirements

- Git
- Docker Engine
- Docker Compose plugin

## Installation

### 1. Clone the repository

```bash
git clone git@github.com:Muhammad-Faizan-Qureshi/django-notes-app-devops.git
cd django-notes-app-devops
```

### 2. Configure environment variables

Create a local `.env` file containing the variables required by `docker-compose.yml`. Never commit real credentials.

### 3. Build and start the application

```bash
docker compose up -d --build
```

### 4. Check container status

```bash
docker compose ps
```

### 5. View logs

```bash
docker compose logs -f
```

### 6. Access the application

Open `http://YOUR_EC2_PUBLIC_IP` in your browser, assuming HTTP traffic on port 80 is allowed by the EC2 security group.

## Nginx

Nginx acts as a reverse proxy, forwarding incoming HTTP requests to Django.

## Learning Goals

- Containerizing a web application
- Running multiple services with Docker Compose
- Connecting Django to MySQL
- Configuring an Nginx reverse proxy
- Deploying and troubleshooting services on AWS EC2

## Security Notes

- Never commit `.env` files, passwords, SSH private keys, or AWS credentials.
- Keep database ports private.
- Use production-ready application server settings for public deployments.
