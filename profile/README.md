# Welcome to the ASAPGaming Project

Once a pioneer in Garry's Mod DarkRP servers. ASAP Gaming was started by CandyApple as a community server where friends could enjoy an authentic roleplay experience. Over the years ASAP became one of the most popular roleplay servers ever to exist on Garry's Mod, holding the top spot for over a year based on BattleMetrics and other sources. ASAP was one of the only DarkRP roleplay servers that offered a completely custom codebase built from the ground up, and introduced new concepts into roleplay unlike any server had done before. As all things must eventually come to an end, ASAP was eventually discontinued to the overall loss of interest in Garry's Mod itself and the project was closed. Nebula Roleplay, a successor to the server was also closed shortly after release due to these reasons.

Here lives the codebase for most of the addons built or enhanced mostly by the lead developer, Gonzo, and contributed to further by Wookie (co-founder of Nebula Roleplay and a backend developer on ASAPGaming). Some addons were taken from the commmunity and further customized to fit the needs of the ASAPGaming architecture. The code is available as open source as a contribution to the community and a testament to the hard work that went into creating an experience like no other and a reminder of all the memories that will stay with many for the years to come. 

# Important Terms

-API: Service which handles operations like logs/player Data/Inventory backend.
-DB: Database which holds all information needed to run all of this.

# Notes

This doesn't bring all features asap had because some scripts were paid, hence not available to publicly release.
In the list we have:

[bluekeypads](https://www.gmodstore.com/market/view/billys-keypads)
[bitminers](https://www.gmodstore.com/market/view/bitminers)
[jewelry](https://www.gmodstore.com/market/view/advanced-jewelry-robbery-another-way-to-earn-money-illegally)
[meth](https://www.gmodstore.com/market/view/zero-s-methlab2-drug-script)
[zero weed growop2](https://www.gmodstore.com/market/view/zero-s-growop-2-weed-script)
[trashman](https://www.gmodstore.com/market/view/zero-s-trashman-trash-script)
[vendingmachine](https://www.gmodstore.com/market/view/zero-s-vendingmachines-shop-script)

Those scripts may not work properly with the gamemode, but if you can provide a proof you bought such scripts, i will share the real script with all integrations on it

# Stuff that you will need

[Lua file that goes inside garrysmod/lua](https://asap.imgonzo.dev/luafiles_asap.zip) (This includes all binaries modules needed for the server)
[DarkRP version that server ran, this goes into gamemodes/](https://asap.imgonzo.dev/darkrp.zip)
[Lua file that goes inside garrysmod/lua](https://asap.imgonzo.dev/addons.7z)

# Usage and Installation

You will need 2 things, a VPS which you can run your database (I highly recommend that over using your panel database).
Alongside this, you will need your game host as well, make sure your host allows you to run:.

[Marketplace repository](https://github.com/ASAPGmod/marketplace)
-Place it wherever you want, don't forget to update [config details](https://github.com/ASAPGmod/marketplace/blob/main/config.js) it with your database.
Make sure to allow port 2052, you can do this by running **ufw allow 2052**.

[Logs Repository](https://github.com/ASAPGmod/logs)
-The same as the marketplace, modify [config details](https://github.com/ASAPGmod/logs/blob/main/config.js) with your database.
Make sure to allow port 2052, you can do this by running **ufw allow 2052**.

[MySQL Driver config](https://github.com/ASAPGmod/driver/blob/main/lua/autorun/server/nebuladriver.lua)
-Set your credentials

Modify Marketplace API endpoint *(This script doesn't have an unique github repo, it's contained in the addons.7z)
asap_marketplace\lua\market\sh_meta.lua
Modify this: asapMarket.API = "http://145.239.205.161:2052" to the service URL your service it's placed, consider it's built into 2052 port.

Modify Logs API endpoint *(Just like marketplace, this script doesn't have a repo, it's inside addons.7z)*
asap-log\lua\logs\api.lua
Modify this: asapLogs.API = "http://145.239.205.161:2053" to the service URL your service it's placed, consider it's built into 2053 port.
asap-log\lua\logs\api.lua

Run as many times server and client as you want, it needs to generate all DBs alone.

-Install the items DB from here: TO BE ADDED

**If you're running locally, you can use this bat file to run the server**
```batch
@echo off
cls
:srcds
start /wait ./srcds.exe +hostname "DEV asap" -condebug -debug -textmode -console -game garrysmod +gamemode darkrp +map rp_downtown_asap_v4_2 +r_hunkalloclightmaps 0 +sv_lan 1 +maxplayers 30 +host_workshop_collection 2886059252 -authkey 83EC77E4B85D6C70EA8830EEA48A093E -tickrate 16 -insecure +insecure
echo (%time%) WARNING: srcds closed or crashed, restarting.
goto srcds
```

# Secondary notes

Everything should just work, if it doesn't just ask for support on Discord: **el.gonzo**.
No, i won't be fixing specific bugs or anything like that, but i will help you to get it launched or improve instructions over it.

# Special thanks

To all our players and our community at ASAPGaming, thank you all for a hell of a run, and thank you to the bad actors too for showing us what we could achieve. We will always be grateful and we'll cherish allt he memories we made.

And special thanks to CodeBlue, the inventory and gobblegums were our stronger part of our gamemode, and we're really proud to have worked with someone like him the short time we could. 🙏

❤
