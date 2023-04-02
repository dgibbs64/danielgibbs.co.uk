---
title: "Minefield: Minecraft Mods, Plugins & Servers Explained"
date: 2021-02-14
categories:
  - gaming
tags:
  - api
  - server
authors:
  - dgibbs
image: /images/minecraft-mods.png
---

> In this post I will be discussing Minecraft: Java Edition exclusively.

_This is part 2 of my articles on Minecraft. Make sure you check out [part 1](https://danielgibbs.co.uk/2021/02/minefield-minecraft-explained/) first._

While Bedrock Edition has simplified how players access custom content, the original and argued by many still the best way to enjoy Minecraft is to use custom game servers and modpacks using Java edition.

As with any mod community, there are many different mods from different developers and several ways of modding your game.

This article will help clear up the difference between Minecraft plugins and mods. For the game servers, what the differences between Bukkit, Spigot and PaperMC are.

## Minecraft Plugins

Plugins are extended features or functionality that can be added to a game server such as new commands, teleport, an economy or factions. A Minecraft player does not require a modded version of the game to access a game server running plugins.

> Plugins are extended features or functionality that can be added to a game server

The advantage of this is that these game servers are easier to access as they don't require a player to download a new game client. An example of a popular plugin is [EssentialsX](https://github.com/EssentialsX/Essentials). There are plenty of articles online that list top plugins.

## Minecraft Mods

Mods are changes to the Minecraft base code that add a whole variety of customisation. This is often customisation that can create fundamental changes in how Vanilla Minecraft works.

![](/images/pixelmon-generations.jpg)

As these are changes to the base code, a custom version of the game client and server is required to play them.

> Mods are changes to the Minecraft base code that add a whole variety of customisation.

Rather than creating a custom game client for every small mod (which would be impractical), developers group their favourite mods together to create _**modpacks**_.

**_Modpacks_** are a group of smaller individual mods that when put together create a new experience for the player. Some modpacks add new features, textures and skins to the existing sandbox. Others create new game modes, add scenarios and objectives.

To make it easier to install modpacks there are special game launchers that can be used to simplify the installation of modpacks. Some of the most popular Include [Technic](https://www.technicpack.net/) and [Feed The Beast](https://feed-the-beast.com/) and [ATLauncher](https://atlauncher.com/). Most modpacks are available from these launchers. An example of a popular modpack is [Pixelmon Generations](https://pixelmongenerations.com/). Like with plugins there are plenty of articles giving there view on the best modpacks available

![](/images/technic-launcher-screenshot.jpg)

Technic Mod Launcher

## Game Servers

![](/images/server.jpg)

When Minecraft was first released it came with a server to allow players to self-host their own Minecraft server. However, many players quickly wanted to extend and add new functionality to their servers.

To do this, custom servers added support for plugins and API's. The first well-known custom server was Bukkit.

> Many players quickly wanted to extend and add new functionality to their servers.

The type of custom game server you want depends upon the type of plugins you want to use. Mods, however, have specially created jar files that can be downloaded. Below is a list of the most well-known Minecraft server software available.

### Vanilla Server

The original unmodified vanilla server is created and distributed by Mojang. This version is considered by many to at times be buggy and laggy with limited options for customisation. But is fine if just getting started with your first Minecraft server.

### Bukkit

[Bukkit](https://dev.bukkit.org/) is the original modded server that added an API allowing developers to create plugins for the server.

![](/images/bukkit.jpg)

### CraftBukkit

CraftBukkit is a modified version of Vanilla that can also run Bukkit plugins. It also includes various performance optimisations over Vanilla. As of today CraftBukkit is mostly only used as a base for Spigot and should not be used.

#### Spigot

![](/images/spigot.png)

[Spigot](https://www.spigotmc.org/) is one of the most popular servers, based on CraftBukkit, it adds further improvements. There are thousands of plugins that work with Spigot making it a top choice for server admins.

### Paper

[Paper](https://papermc.io/) is a high-performance fork of Spigot. It can support the majority of Spigot plugins with a few exceptions, adds various performance improvements and improved API features for plugin developers over Spigot. Because of this Paper has become the most popular modded game server.

### Forge

[Forge](https://forums.minecraftforge.net/) is the server primarily used by modpacks. In most cases, you would not download a vanilla forge server but instead, a custom pre-made modpack server based on forge. An example of a pre-made server is [Tekxit](https://www.technicpack.net/modpack/tekxit-3-official-1122.1253751) from the link you can download both the client and the server versions.

![](/images/forge.jpg)

### BungeeCord

![](/images/bungeecord-en-schema.png)

Source _[EnviousHost](https://www.envioushost.com/blog/how-to-set-up-bungeecord/)_

[BungeeCord](https://github.com/SpigotMC/BungeeCord) is a Minecraft "proxy" server that links Minecraft servers together. BungeeCord server is a gateway that allows players to jump through portals to seamlessly move to different servers.

### Waterfall

[Waterfall](https://github.com/PaperMC/Waterfall) is a fork of the BungeeCord server by the developers of PaperMC. Like with PaperMC is intends to add features, improve stability and performance.
