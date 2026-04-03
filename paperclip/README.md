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

## Quickstart (self-hosted)

No Docker image required. Paperclip uses an interactive CLI onboarding:

```bash
npx paperclipai onboard --yes
```

The wizard walks you through:
1. Database setup (PostgreSQL recommended)
2. Auth configuration
3. Your first company and agents

## Deploy on a VPS / Dokploy

```bash
# On your server
npx paperclipai onboard --yes
```

Then reverse-proxy port `3000` (default) with your Dokploy domain or Nginx/Traefik.

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
