---
published: true
layout: post
title: How to set up a Minecraft server for free without port forwarding [2021]
image: assets/images/Minecraft.jpg
tags: [Mechanical, Keyboard, PC, Gaming]
---

We've all been there. Minecraft servers are somewhat of a hassle to set up, especially if you want it hosted for free, on your own machine. Port forwarding varies from router to router, making it difficult for some people to set it up. And even if you do everything correctly, it may not work. So we wrote this tutorial to solve that problem once and for all - How to host a Minecraft server for free, without port forwarding at all.

This guide includes:
1. Setting up the Minecraft server (skip this step if you already have a working and configured Minecraft server)
2. Setting up playit.gg
3. Configuring the server

## 1. Setting up the Minecraft server
The first step to creating a Minecraft server, is obviously, setting it up.
**Make sure you have the [latest Java SE version installed](https://www.oracle.com/java/technologies/downloads/#jdk17-windows) first.**

**Note: This is not Java 8, this is Java SE 17. If your server closes as soon as you open it, it means that despite being updated to the latest Java 8 version, you still have Java 8.**

Then, head over to the official [Minecraft server download page](https://www.minecraft.net/en-us/download/server) to download the server file for the latest version. If you want older versions, you can check out [mcversions.net](https://mcversions.net/)

Create a new folder for your server (wherever you want) and move the downloaded server file to that folder

Rename the server file to `server` (it should automatically have the `.jar` extension)

Create a new text file and paste the following:
`java -Xmx1024M -Xms1024M -jar server.jar nogui`

After you've pasted that, save the file as `start.bat` in that same directory

Now that you've created a script for starting the server, you can run it. After running it the first time, it will automatically create some files in the same folder and then close. 

You'll see a text file named `eula`. Open the text file, and replace `eula=false` with `eula=true`, save the file, and then you can start the server again.

Congratulations! You have set up a Minecraft server. Other people cannot join it yet, but you can. Open up Minecraft, and in the IP field, type in `localhost`. 

If everything was set up correctly, that should let you join your server! In the next step we will learn how to let other people join it as well.

## 2. Setting up playit.gg
You have a functioning server, but only you can play on it. This is where playit.gg comes in. It's a free service that lets other people join your server, without the need for port forwarding or any other trickery. 

Here's how to set it up:

Download the playit.gg tunnel at [https://playit.gg/download/](https://playit.gg/download)

When you've downloaded it, open it. A console window will pop up, and you will soon be redirected to a website where you can manage the tunnel. 

Make sure to log in first, which you can do only using Discord. If you do not have a Discord account, make sure to head over to [discord.com](https://discord.com/) and create one. 

After you've authenticated with Discord, you can "Add a Tunnel" in the Minecraft Java section. After that's done, you will get an auto-generated IP that should look something like `some-text.auto.playit.gg`. 

Share that IP with your friends, and they should be able to join.

### Note: People will be able to join your server only if you have both playit.gg and the Minecraft server running at the same time.**

That should sum it up for setting up playit.gg. The next step is optional, and that is configuring the server. We'll show you how to set up your server so that people with cracked Minecraft can join, as well as a few other neat options.

## 3. Configuring the server

The server is just a normal survival server now, but you can configure it in many ways, such as allowing people with cracked Minecraft to join, changing world type to flat etc...

Right click on `server.properties`, open it with Notepad.

Now, you can edit and configure whatever you want.

Some notable config values:

| Key         | What it does                                                           | Accepted Values                                         |
|-------------|------------------------------------------------------------------------|---------------------------------------------------------|
| gamemode    | Server gamemode                                                        | survival, creative, adventure, spectator                |
| difficulty  | The difficulty of the server                                           | peaceful, easy, medium, hard                            |
| hardcore    | Whether hardcore mode is on or off                                     | true, false                                             |
| motd        | The description that shows up in the server list                       | Anything, check out https://minecraft.tools/en/motd.php |
| online-mode | Setting it to "false" will allow people with cracked Minecraft to join | true, false                                             |
| pvp         | Whether players can hurt each other                                    | true, false                                             |

You can check out what all of the options do at [minecraft.fandom.com/wiki/Server.properties](https://minecraft.fandom.com/wiki/Server.properties)

Congrats, your Minecraft server should be fully set up and configured! Enjoy your game!

### If it worked, make sure to share this site to other people, if it didn't drop us a mail at support@techtopic.org. We will be more than happy to assist you with any problems you may encounter
