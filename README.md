# Overview

# Usage

Simply deploy with an attached official minecraft [Server jar] as a juju resource:

```
juju deploy /tmp/charm-builds/minecraft-server --resource server-jar=minecraft_server.1.14.jar

juju expose minecraft-server
```

The server runs default on port 25565 in survival mode.

# Configuration
You can set gamemode and server-port like:
```
juju config minecraft-server gamemode='creative'

juju config minecraft-server server-port=12345
```

# Contact Information
Erik Lönroth <erik.lonroth@gmail.com>

## Upstream Project Name

  - Minecraft https://www.minecraft.net
  - Charm code: https://github.com/erik78se/layer-minecraft-server

[Minecraft]: https://www.minecraft.net
[Erik]: http://eriklonroth@wordpress.com
[Server jar]: https://www.minecraft.net/sv-se/download/server/
