# Hub Community Plugins

Curated catalog for Home Lab Hub market.

Default Hub URL:

```
https://raw.githubusercontent.com/opendevtools-org/hub-community-plugins/main/catalog.json
```

Hub lists public plugins from `catalog.json`. Each plugin’s Compose file lives under [`plugins/<id>/`](plugins/).

## Layout

```
catalog.json                 # market index (id, name, install.command, …)
plugins/<id>/docker-compose.yml
plugins/<id>/homelab-plugin.json   # optional
schemas/                     # catalog JSON Schema
```

## Install command

`install.command` is what Hub Market copies. For a community plugin it must:

1. Download `plugins/<id>/docker-compose.yml` into the homelab-deploy folder
2. Add an `include` of that file on `docker-compose.apps.yml` (`project_directory: .`)
3. Recreate the stack with the apps overlay

If `install.command` is omitted and `install.composeFile` is `plugins/<id>/docker-compose.yml`, Hub derives that command.

Private plugins do not belong here (use Hub `market-private.json` on the site).

Published by OpenDevTools.
