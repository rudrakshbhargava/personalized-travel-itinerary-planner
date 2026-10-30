# Claude Code notes

## Project map
- `frontend/`: React + TypeScript + Vite SPA. Routes, page components, Supabase browser auth, API client, and responsive styles live in `frontend/src/`.
- `backend/app/api/routes.py`: REST endpoints; keep handlers small and typed.
- `backend/app/models/schemas.py`: Pydantic schemas and validation.
- `backend/app/services/`: itinerary prompt/generation and budget calculations.
- `backend/app/repositories/store.py`: local SQLite repository and Supabase PostgREST adapter.
- `supabase/migrations/`: production database schema, RLS, indexes, and secure share RPC.
- `docs/`: architecture, database, API, deployment, and activity checklist.

## Critical rules
1. Run tests/type checks/builds after changes and report actual results.
2. Do not change the default demo disclaimer to imply live verification.
3. Do not move AI secrets into browser code or commit `.env` files.
4. Keep Supabase RLS enabled and verify authorization for private trip access.
5. When a user regenerates a trip/day, retain activities marked `is_user_edited`.
6. A share URL must use an unguessable token, expire, be revocable, and return only the intentionally shared read-only subset.

See `AGENTS.md` and `README.md` for exact commands.
