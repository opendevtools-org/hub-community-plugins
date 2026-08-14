# Hub Community Plugins

Curated catalog for Home Lab Hub market.

Default Hub URL:

```
https://raw.githubusercontent.com/opendevtools-org/hub-community-plugins/main/catalog.json
```

Hub lists public plugins from `catalog.json`. Each plugin’s **backend** Compose file lives under [`plugins/<id>/`](plugins/). Web clients live under `plugins/<id>/clients/` plus `docker-compose.frontend.yml`.

## Layout

```
catalog.json
plugins/<id>/docker-compose.backend.yml    # server API (required)
plugins/<id>/docker-compose.frontend.yml   # device web client
plugins/<id>/clients/web/                  # static files + nginx template
plugins/<id>/homelab-plugin.json           # optional
schemas/
```

`docker-compose.yml` may exist as an alias that includes the backend file.

## Backend vs client

| Where | File | Role |
|-------|------|------|
| Server | `docker-compose.backend.yml` | API / workers. Market **Install** copies this into `docker-compose.apps.yml`. |
| Device | `docker-compose.frontend.yml` | Web client. Reverse-proxies to `*_API_UPSTREAM`. Not started on the server. |

If `install.command` is omitted and `install.composeFile` is `plugins/<id>/docker-compose.backend.yml`, Hub derives the backend command. If a client has `composeFile`, Hub derives the device command (standalone `docker compose -f … up`, not the apps overlay).

Private plugins do not belong here (use Hub `market-private.json` on the site).

Published by OpenDevTools.
