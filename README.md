# Cowl

Cowl is a private search engine by [Mist Technologies](https://misttechnologies.net/), powered by [SearXNG](https://github.com/searxng/searxng).

Searches are sent to search engines on your behalf, so they never see your IP address or build a profile on you. No tracking, no ads, and queries are not logged.

This repository contains everything Mist Technologies changed or added on top of the official SearXNG container, published under the AGPL-3.0 as SearXNG's license requires.

## What's here

| File | Purpose |
|---|---|
| `docker-compose.yml` | Runs SearXNG and Valkey. SearXNG is bound to localhost only, behind a reverse proxy. |
| `core-config/settings.yml` | Instance settings: name, bot limiter, public-instance protections, image proxy. |
| `core-config/limiter.toml` | Bot-detection trust settings so the limiter sees real visitor IPs through the proxy. |
| `custom-templates/index.html` | Cowl's custom homepage (logo, name, tagline). |
| `Caddyfile.example` | Example Caddy reverse-proxy config with automatic HTTPS and a noindex header. |
| `.env.example` | Template for environment settings. The real `.env` (with the secret key) is never published. |

## Changes from upstream SearXNG

- Custom homepage template with Cowl branding
- Bot limiter and public-instance protections enabled
- Image proxy enabled
- No other changes to SearXNG's code

## License

AGPL-3.0, the same license as SearXNG. See [LICENSE](LICENSE).

Cowl is an independent instance, not affiliated with the SearXNG project.

Questions: help@misttechnologies.net
Abuse, copyright, or legal reports: abuse@misttechnologies.net
Terms of use: https://misttechnologies.net/cowl/terms/