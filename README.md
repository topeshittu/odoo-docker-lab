# odoo-docker-lab

Multi-version Odoo lab — running Odoo 13, 16, 18, and 19 simultaneously
using Docker, each with isolated PostgreSQL containers and separate port
mappings. Built to support version testing and client migration planning.

## Port mapping
| Version | Odoo port | DB port  |
|---------|-----------|----------|
| Odoo 13 | 8069      | 5432     |
| Odoo 16 | 8070      | 5433     |
| Odoo 18 | 8071      | 5434     |
| Odoo 19 | 8072      | 5435     |

## Usage
\`\`\`bash
cd odoo13 && docker compose up -d
cd odoo16 && docker compose up -d
\`\`\`

## Why this exists
Running multiple Odoo versions simultaneously is a real pain point for
consultants managing clients on different versions. This lab solves it
with isolated containers and clear port separation.
