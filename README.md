# Student Registration Application – Docker Project

A full-stack Student Registration Application containerized with Docker. The project demonstrates how a frontend, backend API, and database can be developed and run as separate services.

## Project Overview

The application is designed to let users register students and view or manage the registered records.

The project focuses on:
- Containerizing application components with Docker
- Building and running services consistently
- Connecting application services through a Docker network
- Managing application configuration with environment variables
- Using Docker Compose to run multiple containers together

## Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React, Vite, JavaScript |
| Backend | Java, Spring Boot, Maven |
| Database | MySQL |
| Containerization | Docker |
| Multi-container orchestration | Docker Compose |
| Version control | Git and GitHub |

> Adjust the technology list if your actual project uses different versions or components.

## Application Architecture

```text
User Browser
    |
    v
Frontend Container
    |
    | HTTP API requests
    v
Backend Container
    |
    | Database connection
    v
MySQL Container
```

Each component runs in its own container. The backend communicates with the database over the Docker network, while the frontend communicates with the backend API.

## Project Structure

The exact directory names may vary depending on the files in this repository.

```text
student-registration-aws/
├── frontend/          # Frontend application
├── backend/           # Spring Boot backend
├── docker-compose.yml # Multi-container configuration (if included)
├── Dockerfile         # Container build instructions (location may vary)
└── README.md
```

## Prerequisites

Install the following tools before running the project:

- Git
- Docker Engine or Docker Desktop
- Docker Compose (or the Docker Compose plugin)

Check the installations:

```bash
git --version
docker --version
docker compose version
```

## Getting the Project

Clone the repository:

```bash
git clone https://github.com/shivraj-kadam/student-registration-docker-aws.git
cd student-registration-docker-aws
```

## Running with Docker Compose

If the repository contains a `docker-compose.yml` file, run the services from the directory containing that file:

```bash
docker compose up -d --build
```

Check running containers:

```bash
docker compose ps
```

View service logs:

```bash
docker compose logs -f
```

Stop the services:

```bash
docker compose down
```

To remove Compose-managed volumes as well (this deletes persisted database data), use:

```bash
docker compose down -v
```

## Useful Docker Commands

Build an image:

```bash
docker build -t student-registration .
```

List running containers:

```bash
docker ps
```

List downloaded or built images:

```bash
docker images
```

View container logs:

```bash
docker logs <container_name>
```

Open a shell inside a running container (when the image includes a shell):

```bash
docker exec -it <container_name> sh
```

## Configuration and Security

- Keep database passwords, API keys, and other secrets out of Git.
- Use environment variables or an untracked `.env` file for local configuration.
- Do not commit private keys, cloud credentials, or production secrets.
- Use a separate example configuration file with placeholder values when documenting required variables.

## Troubleshooting

**Check whether containers are running**

```bash
docker ps -a
```

**Inspect container logs**

```bash
docker compose logs
```

**Check Docker Compose configuration**

```bash
docker compose config
```

**Rebuild the services**

```bash
docker compose up -d --build
```

## Learning Outcomes

Through this project, I practiced:

- Creating and running Docker containers
- Building Docker images
- Writing and using Dockerfiles
- Connecting services through container networking
- Running multiple services with Docker Compose
- Checking container status and logs
- Managing project source code with Git and GitHub

## Author

**Shivraj Kadam**

GitHub: [shivraj-kadam](https://github.com/shivraj-kadam)

## Repository

[Student Registration Docker AWS](https://github.com/shivraj-kadam/student-registration-docker-aws)
