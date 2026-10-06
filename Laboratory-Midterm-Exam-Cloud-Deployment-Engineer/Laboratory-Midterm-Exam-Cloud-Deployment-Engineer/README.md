# Mission 6: The Cloud Deployment Engineer

## Mission Overview

This laboratory activity focuses on deploying a two-tier private cloud storage application using Docker Compose. The stack consists of a Nextcloud web/application container and a MariaDB database container.

> **Academic Integrity Note:** This document is a working student submission template. Review and revise the explanations so they accurately describe your own work and actual observations.

## Objectives

- Explain a multi-tier application architecture.
- Understand the purpose and structure of a `docker-compose.yml` file.
- Use `nano` to create a YAML configuration file.
- Deploy Nextcloud and MariaDB using Docker Compose.
- Document deployment procedures and Infrastructure as Code (IaC) principles using Markdown.
- Maintain a professional GitHub Cloud Computing Portfolio.

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Skills Learned

- Two-tier architecture
- Docker Compose
- YAML configuration
- Linux command-line text editing
- Container networking
- Environment variables
- Infrastructure as Code (IaC)
- Technical documentation
- GitHub portfolio management

## Evidence

The `screenshots/` folder contains the required evidence:

- `compose-deployment.png`
- `nextcloud-web.png`
- `compose-teardown.png`
