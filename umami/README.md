# Umami — Self-hosted Analytics

Privacy-friendly, open source web analytics. No cookies, no tracking, GDPR compliant.

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
| `APP_SECRET` | Random secret string (min 32 chars) — run `openssl rand -hex 32` |

## First Login

Default credentials after deploy:
- User: `admin`
- Password: `umami`

**Change the password immediately after first login.**

## Adding a Website

1. Settings → Websites → Add website
2. Copy the tracking script
3. Paste it in your site's `<head>`

## Links

- [Umami Docs](https://umami.is/docs)
- [GitHub](https://github.com/umami-software/umami)
