# Apache Guacamole (Hub community plugin)

Wrapper around the published image [`flcontainers/guacamole`](https://hub.docker.com/r/flcontainers/guacamole)
(`linux/amd64` and `linux/arm64`). Upstream: [Apache Guacamole](https://guacamole.apache.org/).

Clientless remote desktop gateway: RDP, VNC, and SSH from a browser. The image
bundles the web application, **guacd**, and PostgreSQL on one HTTP port. Hub
does not need a separate device client compose.

Default login: **guacadmin** / **guacadmin**. Change this password on first login.

To reach the Hub host from a connection, use hostname `host.docker.internal`.

## Install

From Hub Market (`/market`), while logged in, click **Installa**.

- The **web client** opens in that same Hub (`/p/guacamole/`).
- The **backend** starts on the Platform server that Hub already points to.

Remote desktop sessions need WebSocket. If a session fails to connect through
`/p/guacamole/`, open the published localhost port (or a dedicated tunnel
hostname pointed at that port).
