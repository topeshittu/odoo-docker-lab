# Odoo Docker Lab

A multi-version Odoo lab environment built with Docker and Docker Compose.

This project demonstrates how to run multiple Odoo versions simultaneously on a single machine while maintaining complete isolation between:

* Odoo containers
* PostgreSQL databases
* Docker volumes
* Docker networks

## Versions Included

| Version | URL                   |
| ------- | --------------------- |
| Odoo 16 | http://localhost:8069 |
| Odoo 18 | http://localhost:8070 |
| Odoo 19 | http://localhost:8071 |

Each version runs in its own Docker Compose project with dedicated PostgreSQL storage and application volumes.

## Features

* Odoo 16, 18 and 19 running side-by-side
* PostgreSQL-backed deployments
* Persistent Docker volumes
* Isolated environments
* Custom addon support
* Reproducible local development environment

## Project Structure

```text
odoo-docker-lab/
├── odoo16/
├── odoo18/
├── odoo19/
└── README.md
```

## Starting Odoo 16

```bash
cd odoo16
docker compose up -d
```

## Starting Odoo 18

```bash
cd odoo18
docker compose up -d
```

## Starting Odoo 19

```bash
cd odoo19
docker compose up -d
```

## Lessons Learned

While building this lab I encountered and resolved:

* Docker volume persistence issues
* Odoo database initialization errors
* Multi-version port conflicts
* Docker Compose project isolation
* PostgreSQL volume management

This repository serves as a repeatable environment for Odoo testing, upgrades, migration planning, and Docker learning.

