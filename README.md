# DecodeLabs Internship — DevOps Engineering Portfolio

Repository containing all projects and assignments completed during my **DevOps Internship at DecodeLabs**.

This portfolio documents my practical learning journey across Linux system administration, Git and GitHub, CI/CD automation, and Docker containerization.

---

## Overview

During the internship, I worked on practical DevOps tasks designed to build a strong foundation in modern software development and operations.

The projects cover:

- Linux System Administration
- Linux Command Line
- Version Control with Git
- GitHub Repository Management
- Branching and Merging
- Merge Conflict Resolution
- Continuous Integration and Continuous Deployment
- GitHub Actions
- YAML Workflow Configuration
- Docker Containerization
- Docker Images and Containers
- Nginx
- Port Mapping
- DevOps Best Practices

---

# Projects

## Project 1 — Linux & Command Line Basics

### Objective

Develop practical proficiency with the Linux command line and understand basic filesystem navigation and file management operations.

### Topics Covered

- Linux filesystem navigation
- Working with directories
- Working with files
- Linux filesystem hierarchy
- Command-line operations
- File and directory manipulation

### Commands Practiced

```bash
pwd
cd
ls
ls -l
ls -a
ls -R
mkdir
mkdir -p
touch
cp
mv
rm
```

### Linux Filesystem Hierarchy

```text
/
├── bin
├── sbin
├── etc
├── var
├── tmp
├── home
└── root
```

### Deliverables

```text
Project-1-Linux/
└── logs/
    └── terminal_execution.txt
```

### Key Learning Outcomes

- Linux command-line proficiency
- Filesystem navigation
- Directory and file management
- Understanding of Linux filesystem structure
- Working with Linux through WSL and Ubuntu

---

## Project 2 — Version Control with Git & GitHub

### Objective

Learn and demonstrate source-code management, change tracking, branching, merging, conflict resolution, and GitHub collaboration workflows.

### Git Concepts

#### Three Trees

```text
Working Tree
     ↓
Staging Area
     ↓
Repository (HEAD)
```

### Git Commands Practiced

```bash
git init
git status
git diff
git add
git commit
git log
git branch
git checkout
git merge
git push
git pull
```

### Skills Demonstrated

- Git repository initialization
- Commit management
- Tracking changes
- Viewing differences
- Creating feature branches
- Switching branches
- Merging branches
- Merge conflict resolution
- Remote repository management
- GitHub workflow
- Pull Request workflow

### Branching Workflow

```text
main
 │
 ├── feature/documentation
 │
 └── feature/conflict-demo
```

### Merge Conflict Resolution

A deliberate merge conflict was created between the main branch and a feature branch by modifying the same section of the README differently.

The conflict was manually resolved before completing the merge.

Example merge history:

```text
*   Merge commit
|| * Feature branch changes
* | Main branch changes
|/
* Previous commits
```

The final history was inspected using:

```bash
git log --oneline --graph --all
```

### Deliverables

```text
Project-2-Version-Control/
└── README.md
```

### Key Learning Outcomes

- Understanding Git version control
- Branch-based development
- Managing project history
- Tracking changes
- Resolving merge conflicts
- Understanding collaborative Git workflows
- Using GitHub for source-code management

---

## Project 3 — CI/CD Pipeline Basics

### Objective

Design and implement a basic automated CI/CD workflow using GitHub Actions.

### Pipeline Architecture

```text
Code
  ↓
Build
  ↓
Lint
  ↓
Test
  ↓
Deploy
```

### Workflow Triggers

```text
push
pull_request
```

### Workflow Stages

```text
Checkout Repository
        ↓
      Build
        ↓
       Lint
        ↓
       Test
        ↓
      Deploy
```

### Workflow Components

#### Events

- `push`
- `pull_request`

#### Jobs

- Build
- Test
- Deployment simulation

#### Steps

- Checkout repository
- Build execution
- Lint checks
- Test execution
- Deployment stage

### Workflow Structure

```text
.github/
└── workflows/
    └── ci-cd-pipeline.yml
```

### Technologies Used

- GitHub Actions
- YAML
- Git
- GitHub

### Key Learning Outcomes

- CI/CD fundamentals
- YAML configuration
- GitHub Actions workflows
- Event-driven automation
- Build and test automation
- Deployment workflow concepts

The CI/CD workflow was successfully executed and verified through GitHub Actions.

---

## Project 4 — Containerization with Docker

### Objective

Learn containerization by packaging and running a web application with its required environment using Docker.

The project demonstrates how containers help solve the **"Works on My Machine"** problem by providing a consistent execution environment.

### Technologies Used

- Docker
- Dockerfile
- Nginx
- HTML
- Linux

### Dockerfile

```dockerfile
FROM nginx:alpine

WORKDIR /usr/share/nginx/html

COPY app/ .

CMD ["nginx", "-g", "daemon off;"]
```

### Docker Concepts Demonstrated

- Base images
- Dockerfile
- Docker build context
- Docker image creation
- Image tagging
- Docker layers
- Layer caching
- WORKDIR
- COPY
- CMD
- Container creation
- Detached mode
- Port mapping
- Container lifecycle
- Nginx web server

### Docker Image

```text
my-app:1.0
```

### Container

```text
my-container
```

### Port Mapping

```text
localhost:8080
       ↓
container:80
```

The application was successfully built into a Docker image and launched as a container.

The application can be accessed through:

```text
http://localhost:8080
```

### Docker Commands Practiced

```bash
docker build -t my-app:1.0 .

docker run -d -p 8080:80 --name my-container my-app:1.0

docker ps

docker images
```

### Project Structure

```text
Project-4-Docker/
├── Dockerfile
├── .dockerignore
├── app/
│   └── index.html
└── screenshots/
```

### Key Learning Outcomes

- Docker fundamentals
- Creating Docker images
- Running Docker containers
- Container networking
- Port forwarding
- Nginx containerization
- Dockerfile configuration
- Understanding containerized applications

---

# Technology Stack

## Operating Systems & Tools

- Linux
- Ubuntu
- Windows Subsystem for Linux (WSL)
- Bash
- Git
- GitHub
- GitHub Actions
- Docker
- Nginx

## Configuration & Automation

- YAML
- Dockerfile
- GitHub Actions

## Concepts

- Linux Filesystem Hierarchy
- Command-Line Operations
- Source Code Management
- Git Branching
- Git Merging
- Merge Conflict Resolution
- Pull Requests
- CI/CD
- GitHub Actions
- Containerization
- Docker Images
- Docker Containers
- Port Mapping
- Layer Caching

---

# Repository Structure

```text
decodelabs_tasks/
│
├── README.md
│
├── Project-1-Linux/
│   └── logs/
│       └── terminal_execution.txt
│
├── Project-2-Version-Control/
│   └── README.md
│
├── .github/
│   └── workflows/
│       └── ci-cd-pipeline.yml
│
└── Project-4-Docker/
    ├── Dockerfile
    ├── .dockerignore
    ├── app/
    │   └── index.html
    └── screenshots/
```

---

# Skills Acquired

## Linux

- Filesystem navigation
- File and directory management
- Linux command-line usage
- Bash fundamentals
- Linux filesystem structure
- Working with Linux through WSL

## Git & GitHub

- Repository initialization
- Commit management
- Change tracking
- Branching
- Merging
- Merge conflict resolution
- Git history management
- Remote repositories
- Pull Requests
- GitHub workflows

## CI/CD

- GitHub Actions
- YAML workflow configuration
- Automated workflows
- Build stages
- Lint stages
- Testing stages
- Deployment concepts
- Event-driven automation

## Docker

- Dockerfiles
- Docker images
- Docker containers
- Image tagging
- Nginx
- Port mapping
- Container networking
- Container lifecycle management
- Layer caching

---

# Learning Progression

```text
Linux Fundamentals
        ↓
Git & GitHub
        ↓
CI/CD Automation
        ↓
Docker Containerization
```

This progression helped build practical knowledge from basic system operations to automated software delivery and containerized applications.

---

# Future Learning Path

Future areas of learning include:

- Advanced Docker
- Docker Compose
- Kubernetes
- AWS Cloud Services
- Infrastructure as Code (IaC)
- Terraform
- Cloud Networking
- Monitoring & Logging
- Advanced CI/CD Pipelines
- DevSecOps

---

# Author

## Jay Mehta

**DevOps Intern**

This repository contains practical projects completed during my DecodeLabs internship as part of my journey toward developing real-world DevOps and cloud engineering skills.
