# Indiemaker Tools 🛠️

A collection of self-hosted, open source tools for indie makers — deployable on Dokploy or any Docker-compatible server.

No vendor lock-in. No monthly SaaS fees. Your data, your server.

## Tools included

| Tool | Category | Description |
|---|---|---|
| [Umami](./umami) | Analytics | Privacy-friendly web analytics — Google Analytics alternative |
| [Listmonk](./listmonk) | Email Marketing | Self-hosted newsletter & mailing list manager |

## Requirements

- A server with Docker + Docker Compose
- [Dokploy](https://dokploy.com) (recommended) or any Docker host
- A domain with DNS access

## Quick Start

Each tool lives in its own folder with:
- `docker-compose.yml` — ready to paste into Dokploy
- `.env.example` — environment variables to configure
- `README.md` — setup instructions

## Contributing

PRs welcome. If you have a self-hosted tool that fits the indie maker stack, open an issue.

## License

MIT
