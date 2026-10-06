# Base44 Dev Environment

## Project Overview
Static HTML portfolio site ("PERSPECTIVES" by Joshua Hart). Single `index.html` with inline CSS, plus `artist.jpeg` and `voice.mp3` assets. No backend, no database, no build step.

## Running the App
```bash
docker compose -f docker-compose.base44.yml up -d
```
- Served by nginx:alpine on host port 3000.
- Source is bind-mounted read-only at `/usr/share/nginx/html` — edits to `index.html` or assets are reflected immediately (no rebuild needed). Call `reload_preview` after edits to force a browser refresh.

## Notes
- The original HTML referenced `artist.png` but the file is `artist.jpeg`; the src was corrected during setup.
- No secrets or external credentials required.
