# Odoo Docker Lab

A multi-version Odoo lab environment built with Docker and Docker Compose.

This repository demonstrates how to run multiple Odoo versions simultaneously on a single machine while keeping each deployment fully isolated with its own:

* Odoo container
* PostgreSQL container
* Docker volumes
* Docker network
* Docker Compose project

## Included Versions

| Version | URL                   |
| ------- | --------------------- |
| Odoo 16 | http://localhost:8069 |
| Odoo 18 | http://localhost:8070 |
| Odoo 19 | http://localhost:8071 |

## Project Structure

```text
odoo-docker-lab/
├── odoo16/
│   └── docker-compose.yml
├── odoo18/
│   └── docker-compose.yml
├── odoo19/
│   └── docker-compose.yml
└── README.md
```

## Features

* Multi-version Odoo deployments
* Docker Compose based setup
* PostgreSQL-backed databases
* Persistent Docker volumes
* Isolated environments for each version
* Side-by-side version testing
* Migration and upgrade lab environment

## Running Odoo 16

```bash
cd odoo16
docker compose up -d
```

Access:

```text
http://localhost:8069
```

## Running Odoo 18

```bash
cd odoo18
docker compose up -d
```

Access:

```text
http://localhost:8070
```

## Running Odoo 19

```bash
cd odoo19
docker compose up -d
```

Access:

```text
http://localhost:8071
```

## What I Learned

Building this lab provided hands-on experience with:

* Docker image management
* Docker Compose orchestration
* PostgreSQL containers
* Persistent volume management
* Multi-container application deployment
* Container networking
* Port mapping and service isolation
* Troubleshooting Odoo startup and database initialization issues

## Use Cases

* Testing different Odoo versions locally
* Learning Docker and container orchestration
* Comparing version behavior
* Preparing for Odoo upgrades and migrations
* Creating reproducible development environments

## Technologies

* Docker
* Docker Compose
* Odoo 16
* Odoo 18
* Odoo 19
* PostgreSQL 15

