# Overview
[Minecraft] is the ever so popular game. This charm deploys a stand alone minecraft server for you.

You have to download the [Server jar] first, which when you attach as a resource.

# Usage

* Start by downloading the official [Server jar].

* Deploy with the server jar as a juju resource:

```
juju deploy cs:~erik-lonroth/minecraft-server --resource server-jar=minecraft_server.1.14.jar

juju expose minecraft-server
```

The server runs default on port 25565 in survival mode.

# Operating the server
The charm sets up a 'screen' session named 'minecraft' as the user minecraft. 
You can attach to this at any time to operate the server.

For example:
```
juju ssh minecraft-server/0

sudo -u minecraft screen -R minecraft

# ctrl-a d (Gets you out)
```


# Configuration
You can set gamemode and server-port like this:
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
