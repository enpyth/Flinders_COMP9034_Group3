# Farming Time Management PoC

## Quick start

```bash
./init.sh
pnpm run dev
```

## Monorepo apps

- `apps/web`: Next.js frontend shell
- `apps/api`: Express + TypeScript API
- `packages/shared`: shared contracts and enums

## Backend docs and scripts

- Swagger UI: `http://localhost:4000/api/v1/docs`
- OpenAPI JSON: `http://localhost:4000/api/v1/openapi.json`
- Supabase integration status (admin): `GET /api/v1/integrations/supabase/status`
- Run DB migrations (Postgres mode):

```bash
pnpm --filter @farm/api run migrate
```

- Seed fake data into local Supabase Postgres (`DB_URL` or `DATABASE_URL`):

```bash
pnpm --filter @farm/api run seed
```

- SQL files:
  - `apps/api/db/clean_create.sql` (drop + create schema)
  - `apps/api/db/seed.sql` (fake data inserts)
- Seed login password for inserted users: `SeedPass123!`

## Environment

Copy `.env.example` to `.env` when you need overrides. Defaults are usable for local startup.
