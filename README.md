# GTO Wizard Clone - Scaffold

Minimal scaffold: React + TypeScript frontend, Node/Express backend with a mock solver endpoint, Dockerfiles and docker-compose for local dev.

## Quick start (local)

1. Copy repository to `gto-clone/`.
2. Create `.env` from `.env.example` and set values.
3. Start with Docker Compose (recommended):

```bash
# from repo root
docker-compose up --build
```

Frontend will be at http://localhost:3000 and API at http://localhost:4000.

## What is included

- Frontend: React + TypeScript with a small `RangeEditor` component and a mock UI to submit a solve request.
- Backend: Express server with `/api/solve` (creates a job) and `/api/solve/:id` (status/result). A simple in-memory job store simulates solving.
- Dockerfiles + docker-compose for easy development.

## Next steps

- Replace the mock solver with a real WASM or server solver binary.
- Add auth, billing, persistent DB, and job queue (Redis + BullMQ or Celery).
- Expand frontend with trainer, hand history importer, and range visualizer.
