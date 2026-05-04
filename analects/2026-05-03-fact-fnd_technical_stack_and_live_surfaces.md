---
status: draft
audience: [yc, technical, investor]
tags: [tech_stack, MyCite, portal, infrastructure, Rust, Python, deployment]
related: [2026-00-00-fact-technical_skills, 0000-00-00-fragment-fnd_ai_assisted_development_workflow]
---

# FND technical stack and live surfaces

## Fact

FND's technical stack includes:

- Python
- Flask
- REST APIs
- PostgreSQL/SQL
- SQLite where appropriate
- pandas for ETL
- BeautifulSoup for parsing
- Bash
- Docker / Docker Compose
- NGINX
- Gunicorn
- systemd
- AWS EC2
- AWS Route 53
- Linux
- Git
- HTML/CSS/JavaScript
- Rust / Cargo workspace for local agent tooling

## Live technology surfaces

The MyCite/FND system includes:

- a live portal shell;
- canonical `/portal` routing;
- `/portal/api/v2/...` admin/API surfaces;
- SQL-backed authority surfaces;
- SYSTEM / NETWORK / UTILITIES portal roots;
- Workbench UI for SQL-backed authority inspection;
- AWS-CSM service tooling;
- FND-DCM service tooling;
- NGINX as public ingress;
- localhost-bound internal services;
- oauth2-proxy and Keycloak for gated portal access;
- systemd/Gunicorn portal services;
- deployment-truth infrastructure repo.

## YC stack posture

The stack answer should not sound like a generic list of languages. It should show that the founder can build, deploy, and operate the full system:

> I write the product code, runtime contracts, deployment scripts, service configuration, data normalization tooling, and infrastructure myself.
