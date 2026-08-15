# WebSSH (Hub community plugin)

Wrapper around the published image [`austozi/webssh`](https://hub.docker.com/r/austozi/webssh)
(`linux/amd64` and `linux/arm64`). Upstream: [`huashengdun/webssh`](https://github.com/huashengdun/webssh) (MIT).

Browser SSH client (password, public key, TOTP). The web UI is in the same container; Hub does not need a separate device client compose.

To SSH into the Hub host from the plugin, use hostname `host.docker.internal`.

## Install

From Hub Market (`/market`), while logged in, click **Installa**.

- The **web client** opens in that same Hub (`/p/webssh/`).
- The **backend** starts on the Platform server that Hub already points to.
