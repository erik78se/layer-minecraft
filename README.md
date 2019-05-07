# Overview
[Minecraft] is the ever so popular game. This charm deploys a stand alone minecraft server for you.

You have to download the [server jar] first, which you attach as a resource.

The server needs about 2GB ram and 2 cpus to be happy (might need more).

# Usage

* Start by downloading the official [server jar].

* Deploy with the server jar as a juju resource:

```bash
juju deploy cs:~erik-lonroth/minecraft-server --constraints "mem=2G cores=2" --resource server-jar=minecraft_server.1.14.jar

juju expose minecraft-server
```

You can attach a server-jar after deploy also with [juju attach-resource] if you like to upgrade later for example.
```bash
juju attach-resource minecraft-server server-jar=minecraft_server.1.14.jar
```

The server runs default on port 25565 in survival mode.

# Configuration
All configuration changes triggers a server restart.

Example, set gamemode and server-port like this:
```bash
juju config minecraft-server gamemode='creative' server-port=12345
```

# Operating the server
The charm sets up a 'screen' session named 'minecraft' as the user minecraft. 
You can attach to this at any time to operate the server.

For example:
```bash
juju ssh minecraft-server/0

sudo -u minecraft screen -R minecraft

# ctrl-a d (Gets you out)
```

# Contact Information
Erik Lönroth <erik.lonroth@gmail.com>

## Upstream Project Name

  - Minecraft https://www.minecraft.net
  - Charm code: https://github.com/erik78se/layer-minecraft-server

[Minecraft]: https://www.minecraft.net
[Erik]: http://eriklonroth@wordpress.com
[server jar]: https://www.minecraft.net/sv-se/download/server/
[juju attach-resource]: https://docs.jujucharms.com/2.5/en/charms-resources
