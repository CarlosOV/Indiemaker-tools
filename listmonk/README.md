# Listmonk — Self-hosted Newsletter & Mailing Lists

High performance, self-hosted newsletter and mailing list manager.

## Deploy on Dokploy

1. Create a new **Docker Compose** service in Dokploy
2. Paste the contents of `docker-compose.yml`
3. Add your environment variables (see `.env.example`)
4. Set your domain in Dokploy → Domains
5. Deploy

## Environment Variables

| Variable | Description |
|---|---|
| `POSTGRES_DB` | Database name |
| `POSTGRES_USER` | Database user |
| `POSTGRES_PASSWORD` | Strong password for the database |
| `TIMEZONE` | Your timezone (e.g. `America/Lima`, `Europe/Madrid`) |

## First Login

Default credentials after deploy:
- User: `admin`
- Password: `listmonk`

**Change the password immediately after first login.**

## Setup Email Sending

1. Settings → SMTP
2. Configure your SMTP provider (Amazon SES, Mailgun, Resend, etc.)
3. Send a test email to verify

## Links

- [Listmonk Docs](https://listmonk.app/docs)
- [GitHub](https://github.com/knadh/listmonk)
