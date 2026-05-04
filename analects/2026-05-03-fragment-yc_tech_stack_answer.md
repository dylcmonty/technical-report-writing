---
status: draft
audience: [yc]
tags: [yc_application, tech_stack, ai_tools]
related: [2026-05-03-fact-fnd_technical_stack_and_live_surfaces]
---

# YC tech stack answer

FND uses Python, Flask, REST APIs, PostgreSQL/SQL, SQLite where appropriate, pandas for ETL, BeautifulSoup for parsing, Bash, Docker/Docker Compose, NGINX, Gunicorn, systemd, AWS EC2, Route 53, Linux, Git, HTML, CSS, and JavaScript.

The current MyCite/FND infrastructure includes a live portal shell, SQL-backed authority surfaces, structured runtime contracts, portal APIs, NGINX ingress, oauth2-proxy, Keycloak, Redis, and service deployment tooling. I also maintain Rust tooling for local agent workflows through a Cargo workspace with runtime/session/config/tooling code, provider/client code, MCP/tool support, and OpenAI-compatible local provider support.

I use ChatGPT, Claude, and coding-agent workflows for code generation, refactoring, review, debugging, documentation, repo management, and structured task decomposition. I still review, test, and commit the product code myself.
