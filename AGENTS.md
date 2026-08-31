# Base44 Dev Environment

## Overview
This is a static HTML site (single `index.html` plus media assets). No build step, no backend, no package manager.

## Running
```
docker compose -f docker-compose.base44.yml up -d
```
Serves `index.html` and assets via nginx on host port 3000. Source is bind-mounted read-only, so edits to `index.html` appear on the next request (no rebuild needed).

## Verifying
- `curl -sf http://localhost:3000/` returns the HTML page.
- Preview is served through an external hostname; nginx serves by host so no allowlist config is needed.

## Secrets
None required.
