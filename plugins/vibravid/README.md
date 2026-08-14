# VibraVid (Hub community plugin)

Wrapper around the published image [`ghcr.io/astraelabs/vibravid`](https://github.com/AstraeLabs/VibraVid).
License of the upstream project: GPL-3.0.

Default UI: `http://SERVER:3100/` (override with `VIBRAVID_PORT`).

This software is for lawful personal use of content you have rights to process.
It does not include DRM keys, CDMs, or circumvention tooling.

## Install

Copy the command from Hub Market (`/market`), or from `catalog.json` `install.command`.
Run it in the homelab-deploy folder (flat clone or site instance). It:

1. Writes `plugins/vibravid/docker-compose.yml`
2. Includes that file from `docker-compose.apps.yml`
3. Starts the stack with the apps overlay

Then merge [`.env.example`](./.env.example) into the site `.env` and recreate:

```bash
docker compose -f docker-compose.yml -f docker-compose.lan.yml -f docker-compose.apps.yml up -d
```
