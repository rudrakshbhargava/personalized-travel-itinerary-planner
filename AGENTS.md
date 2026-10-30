# Agent instructions

This repository is a React + TypeScript + Vite frontend and a FastAPI backend for a personalized travel itinerary planner.

## Before changing code
- Inspect the affected files and preserve unrelated work.
- Keep demo data clearly labelled. Do not fabricate live attraction data, prices, opening hours, ratings, routing, reservations, or availability.
- Never place backend secrets in frontend `VITE_` variables, committed files, tests, documentation examples, or logs.
- Every private trip operation must enforce authenticated ownership. Supabase Row Level Security is required for deployed private data.
- Preserve manually edited activities when regenerating suggestions.

## Commands
- Frontend: `cd frontend && npm install && npm run typecheck && npm run lint && npm test && npm run build`
- Backend: `cd backend && python -m venv .venv && . .venv/bin/activate && pip install -r requirements.txt && ruff check app tests && pytest -q`
- Local demo: start the backend with `DEMO_MODE=true`, then run the frontend with `VITE_API_BASE_URL=http://localhost:8000`.

## Code conventions
- TypeScript strict mode; reusable UI and service functions; meaningful accessibility labels.
- FastAPI handlers validate through Pydantic and delegate persistence and generation to service/repository modules.
- Tests must not depend on live AI, Supabase, maps, or paid APIs.
- Report checks as verified only if the command actually ran.
