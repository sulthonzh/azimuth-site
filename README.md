# azimuth-site

Landing page and documentation for [azimuth](https://azimuth.my.id) — the OS that doesn't let apps run wild.

## Structure

- `index.html` — the landing page
- `docs/` — documentation (markdown, rendered by the docs site)

## Deployment

The site is served from svr1 via Docker + Traefik + Let's Encrypt:

```bash
# On svr1, the container is already running:
docker ps | grep azimuth-site

# To update the landing page:
# 1. Edit index.html in this repo
# 2. Copy to svr1: scp index.html svr1:/srv/apps/azimuth-site/
# 3. Restart: ssh svr1 "cd /srv/apps/azimuth-site && docker compose restart site"
```

## License

MIT — same as the kernel.