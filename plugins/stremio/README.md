# Stremio (Hub community plugin)

Wrapper around the published image [`tsaridas/stremio-docker`](https://github.com/tsaridas/stremio-docker) (MIT).
Upstream product: [Stremio](https://www.stremio.com/).

The image bundles **Stremio Web** and the **streaming server** on a single HTTP port (8080). Hub does not need a separate device client compose.

This software is for lawful personal use of content you have rights to play.
It does not include DRM keys, CDMs, or circumvention tooling.

## Install

From Hub Market (`/market`), while logged in, click **Installa**.

- The **web client** opens in that same Hub (`/p/stremio/`).
- The **backend** starts on the Platform server that Hub already points to.

Optional GPU transcoding on Linux: pass `/dev/dri` into the container (see upstream README). Not enabled by default.
