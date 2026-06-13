# Odoo Multi-Version Containerized Environment

## Overview

This repository provides a containerized multi-version Odoo environment designed for deployment validation, upgrade testing, migration planning, and operational comparison across multiple Odoo releases.

The environment enables Odoo 16, Odoo 18, and Odoo 19 to run simultaneously on a single host while maintaining complete isolation between application services, databases, storage, and networking components.

Each deployment operates independently and can be managed, upgraded, or removed without affecting other environments.

---

## Objectives

The primary objectives of this project are:

* Standardize Odoo deployments using containerization.
* Enable side-by-side execution of multiple Odoo versions.
* Provide isolated environments for testing and validation.
* Simplify upgrade and migration planning.
* Establish reproducible deployment workflows.

---

## Environment Architecture

Each Odoo version consists of:

### Application Layer

* Dedicated Odoo container
* Version-specific runtime environment
* Independent service lifecycle

### Database Layer

* Dedicated PostgreSQL container
* Isolated database instance
* Independent data management

### Storage Layer

* Persistent Docker volumes
* Data retention across container recreation
* Separation of application lifecycle and storage

### Network Layer

* Dedicated Docker network
* Service isolation
* Internal container communication

---

## Deployment Topology

```text
Host Machine
│
├── Odoo 16 Environment
│   ├── Odoo Container
│   ├── PostgreSQL Container
│   ├── Persistent Volumes
│   └── Dedicated Network
│
├── Odoo 18 Environment
│   ├── Odoo Container
│   ├── PostgreSQL Container
│   ├── Persistent Volumes
│   └── Dedicated Network
│
└── Odoo 19 Environment
    ├── Odoo Container
    ├── PostgreSQL Container
    ├── Persistent Volumes
    └── Dedicated Network
```

---

## Available Environments

| Version | Endpoint              |
| ------- | --------------------- |
| Odoo 16 | http://localhost:8069 |
| Odoo 18 | http://localhost:8070 |
| Odoo 19 | http://localhost:8071 |

---

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

---

## Deployment

### Odoo 16

```bash
cd odoo16
docker compose up -d
```

### Odoo 18

```bash
cd odoo18
docker compose up -d
```

### Odoo 19

```bash
cd odoo19
docker compose up -d
```

---

## Operational Capabilities

* Multi-version Odoo deployment management
* Environment isolation
* PostgreSQL-backed persistence
* Independent service lifecycle management
* Side-by-side version validation
* Upgrade and migration testing
* Reproducible infrastructure deployment
* Container-based operational consistency

---

## Use Cases

### Upgrade Planning

Validate application behavior between Odoo releases before production upgrades.

### Migration Testing

Evaluate migration paths and compatibility requirements across versions.

### Deployment Standardization

Establish repeatable deployment procedures using Docker Compose.

### Environment Validation

Compare functionality, configuration, and performance across Odoo releases.

### Operational Testing

Test backup, recovery, upgrade, and maintenance procedures in isolated environments.

---

## Technologies

* Docker
* Docker Compose
* Odoo 16
* Odoo 18
* Odoo 19
* PostgreSQL 15
* Linux

---

## Outcome

Delivered a reproducible multi-version Odoo deployment environment capable of supporting version validation, migration planning, and operational testing while maintaining complete workload isolation through containerization.

The architecture provides a practical foundation for managing and evaluating Odoo deployments using modern container-based infrastructure practices.

