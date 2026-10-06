# Base44 Dev Environment

## Project Overview
This is a single static HTML page (`Index.html`) — a marketing/info guide for True Form Construction about legal basement suite requirements in Ontario. No build step, no backend, no external dependencies.

## Running the App
```
docker compose -f docker-compose.base44.yml up -d
```
- Served by nginx on host port 3000.
- The repo is bind-mounted read-only into the container, so edits to `Index.html` are reflected immediately — call `reload_preview` after changes so the user sees them.

## Verification
- `curl -s http://localhost:3000/` should return the HTML page (title: "Legal Basement Suite Requirements in Ontario").
- Healthcheck: nginx responds on `/`.
