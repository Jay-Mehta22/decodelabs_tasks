DevOps Engineering Portfolio
Overview

This repository contains the projects completed during my DevOps Internship at DecodeLabs. The portfolio documents my progression from Linux fundamentals and version control to CI/CD automation and containerization, providing practical experience with tools and workflows commonly used in modern software development and operations.

The projects focus on building a strong foundation in:

    Linux System Administration
    Version Control with Git and GitHub
    Continuous Integration and Continuous Deployment (CI/CD)
    Containerization with Docker
    DevOps Best Practices
    Software Development Lifecycle (SDLC)

Technology Stack
Operating Systems & Tools

    Linux
    Bash Shell
    Git
    GitHub
    GitHub Actions
    Docker

Configuration & Automation

    YAML
    Dockerfile

Concepts

    Linux Filesystem Hierarchy Standard (FHS)
    Source Code Management
    Branching Strategies
    Pull Requests
    CI/CD Pipelines
    Containerization
    Layer Caching
    Port Mapping

Project 1: Linux & Command Line Basics
Objective

Transition from graphical user interface (GUI) interactions to efficient command-line operations and low-level system management.
Skills Demonstrated
Filesystem Navigation

    pwd
    cd
    ls
    ls -l
    ls -a
    ls -R

File & Directory Management

    mkdir
    mkdir -p
    touch
    cp
    mv
    rm

Linux Filesystem Hierarchy Standard (FHS)

Explored and understood critical Linux directories:

/
├── bin
├── sbin
├── etc
├── var
├── tmp
├── home
└── root

Deliverables

Project-1-Linux/
└── logs/
    └── terminal_execution.txt

Key Learning Outcomes

    Linux command-line proficiency
    Directory structure management
    System navigation techniques
    Understanding of Linux architecture

Project 2: Version Control with Git
Objective

Implement source code management, change tracking, collaboration workflows, and repository synchronization using Git and GitHub.
Core Concepts
The Three Trees
Working Tree

Local development workspace.
Staging Area (Index)

Area where changes are prepared before commit.
Repository (HEAD)

Permanent history of committed changes.
Git Commands Used

git init
git status
git diff
git add
git commit
git branch
git checkout
git merge
git push
git pull

Skills Demonstrated

    Repository initialization
    Commit management
    Branch creation
    Branch merging
    Pull Request workflow
    Conflict resolution
    Remote repository management

Deliverables

A GitHub repository containing:

    Multiple commits
    Feature branches
    Pull Requests
    Merge history
    Conflict resolution examples

Key Learning Outcomes

    Collaborative development workflows
    Version control best practices
    Source code traceability
    GitHub repository management

Project 3: CI/CD Pipeline Basics
Objective

Design and implement automated workflows that build, test, and validate code through Continuous Integration and Continuous Deployment principles.
Pipeline Architecture

Code
  ↓
Build
  ↓
Test
  ↓
Deploy

GitHub Actions Workflow
Workflow Components
Events

    push
    pull_request

Jobs

    Build
    Test
    Deployment simulation

Steps

    Checkout repository
    Build execution
    Lint checks
    Test execution
    Deployment stage

Deliverables

.github/
└── workflows/
    └── ci-cd-pipeline.yml

Key Learning Outcomes

    Workflow automation
    YAML configuration
    Event-driven pipelines
    Continuous Integration concepts
    Continuous Deployment fundamentals

Project 4: Containerization with Docker
Objective

Solve the "Works on My Machine" problem by packaging applications and dependencies into portable, predictable containers.
Containerization Lifecycle
Phase 1: Blueprint Creation

Created:

Dockerfile
.dockerignore

Dockerfile Components

FROM nginx:alpine
WORKDIR /usr/share/nginx/html
COPY app/ .
CMD ["nginx", "-g", "daemon off;"]

Concepts Learned

    Base Images
    Docker Layers
    WORKDIR
    COPY
    CMD
    ENTRYPOINT
    Build Context Optimization

Phase 2: Image Building

Built Docker images using:

docker build -t my-app:1.0 .

Concepts Learned

    Docker Images
    Layer Caching
    Image Tagging
    Build Optimization

Phase 3: Container Deployment

Executed containers using:

docker run -d -p 8080:80 --name my-container my-app:1.0

Concepts Learned

    Detached Mode (-d)
    Port Mapping (-p)
    Container Networking
    Container Lifecycle Management

Deliverables

Project-4-Docker/
├── Dockerfile
├── .dockerignore
├── app/
│   └── index.html
└── screenshots/

Key Learning Outcomes

    Docker fundamentals
    Image creation
    Container deployment
    Networking and port forwarding
    Environment consistency

Repository Structure

.
├── README.md
├── Project-1-Linux/
│   └── logs/
│       └── terminal_execution.txt
│
├── Project-2-Version-Control/
│
├── .github/
│   └── workflows/
│       └── ci-cd-pipeline.yml
│
└── Project-4-Docker/
    ├── Dockerfile
    ├── .dockerignore
    ├── app/
    └── screenshots/

Skills Acquired
Linux

    Filesystem navigation
    File operations
    System structure understanding

Git & GitHub

    Version control
    Branching strategies
    Pull Requests
    Merge conflict resolution

CI/CD

    GitHub Actions
    Workflow automation
    Pipeline design

Docker

    Containerization
    Image creation
    Container deployment
    Networking

Future Learning Path

Upcoming areas of focus include:

    Advanced Docker
    Docker Compose
    Kubernetes
    AWS Cloud Services
    Infrastructure as Code (IaC)
    Monitoring and Logging
    Advanced CI/CD Pipelines
