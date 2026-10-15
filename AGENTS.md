# AGENTS.md

## Project overview
Single static HTML landing page (`index.html`) for GreenDildoCoin ($GDC), a parody memecoin. No backend, no build step, no dependencies.

## Running the app
- Served by nginx (alpine) via `docker-compose.base44.yml`, mapped to host port 3000.
- The repo `index.html` is bind-mounted into the container, so edits appear on refresh without rebuilding.
- Start: `docker compose -f docker-compose.base44.yml up -d`
- Healthcheck: nginx responds to `GET /` (HTTP 200).

## No secrets required
This project has no external service dependencies.
