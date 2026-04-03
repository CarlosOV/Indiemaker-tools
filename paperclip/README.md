# Paperclip — AI Company Orchestration

> "If an AI agent is an employee, Paperclip is the company."

Open-source platform to run autonomous AI companies. Hire agents, set goals, assign budgets, and manage everything from a single dashboard — like a task manager, but the employees are AI.

## What it does

- **Org chart** — CEO, CTO, engineers, marketers. Hierarchies, roles, reporting lines.
- **Goal alignment** — Every task traces back to the company mission.
- **Heartbeats** — Agents wake on a schedule, check work, and delegate up/down the org chart.
- **Cost control** — Monthly budgets per agent. When they hit the limit, they stop.
- **Multi-company** — One deployment, many companies. Full data isolation.
- **Audit log** — Every decision explained. Full tool-call tracing.
- **Mobile ready** — Monitor and manage from your phone.

## Deploy on Dokploy

1. Create a PostgreSQL database in Dokploy → Database
2. Create a new **Docker Compose** service
3. Paste the contents of `docker-compose.yml`
4. Set environment variables (see `.env.example`)
5. Set your domain in Dokploy → Domains → port `3100`
6. Deploy

## Deploy with Docker (generic)

```bash
docker build -t paperclip .
docker run -d \
  -e DATABASE_URL=postgresql://user:password@host:5432/paperclip \
  -e SERVE_UI=true \
  -p 3100:3100 \
  paperclip
```

## Environment Variables

Set via the onboard wizard or manually:

| Variable | Description |
|---|---|
| `DATABASE_URL` | PostgreSQL connection string |
| `NEXTAUTH_SECRET` | Random secret for auth sessions |
| `NEXTAUTH_URL` | Your public URL (e.g. `https://agents.yourdomain.com`) |
| `OPENAI_API_KEY` | Or any other LLM provider key |

## Bring Your Own Agent

Paperclip works with any agent that can receive a heartbeat:
- OpenClaw
- Claude / Cursor / Codex
- Custom agents via API

## Links

- [GitHub](https://github.com/paperclipai/paperclip)
- [Docs](https://paperclip.ing/docs)
- [Discord](https://discord.gg/m4HZY7xNG3)
