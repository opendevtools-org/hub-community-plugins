# VibraVid (Hub community plugin)

Wrapper around the published image [`ghcr.io/astraelabs/vibravid`](https://github.com/AstraeLabs/VibraVid).
License of the upstream project: GPL-3.0.

**Backend** (server): `docker-compose.backend.yml` — default `http://SERVER:3100/`
**Web client** (device): `docker-compose.frontend.yml` — default `http://127.0.0.1:3180/`

This software is for lawful personal use of content you have rights to process.
It does not include DRM keys, CDMs, or circumvention tooling.

## Install

From Hub Market (`/market`), while logged in, click **Installa**.

- The **web client** opens in that same Hub (`/p/vibravid/`).
- The **backend** starts on the Platform server that Hub already points to.

Optional: `docker-compose.frontend.yml` if you want a standalone reverse-proxy client without Hub.
