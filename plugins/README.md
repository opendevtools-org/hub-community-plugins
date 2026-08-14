# Community plugins

Each folder is one Home Lab Hub market plugin. Hub reads the index
[`catalog.json`](../catalog.json).

```
plugins/<id>/
  docker-compose.backend.yml     # required — server API, prebuilt image
  docker-compose.frontend.yml    # web client for devices
  clients/web/                   # nginx template + launcher page
  homelab-plugin.json            # optional
  .env.example                   # vars to merge into the site `.env`
```

## Backend (server)

Market **Install** downloads `docker-compose.backend.yml` and includes it from
`docker-compose.apps.yml`.

## Web client (device)

Market **Client** downloads `docker-compose.frontend.yml` plus `clients/web/`
and runs that compose on the device, with `*_API_UPSTREAM` pointing at the server.

Do not put secrets in this repo. Site owners set them in their `.env`.
