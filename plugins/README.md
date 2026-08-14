# Community plugins

Each folder is one Home Lab Hub market plugin. Hub reads the index
[`catalog.json`](../catalog.json); `install.composeFile` points here.

```
plugins/<id>/
  docker-compose.yml    # required — prebuilt image, no host build
  homelab-plugin.json   # optional — Hub agent manifest
  .env.example          # optional — vars to merge into the site `.env`
```

## Install (homelab-deploy)

The catalog `install.command` (copied from Hub Market):

1. Downloads `plugins/<id>/docker-compose.yml` into the site folder.
2. Appends an `include` entry to `docker-compose.apps.yml`.
3. Runs the usual three-file Compose (`docker-compose.yml` + lan/local + apps).

Do not put secrets in this repo. Site owners set them in their `.env`.
