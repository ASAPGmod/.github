# Welcome to ASAPGaming Project

Server it's not really coming back but fuck that, anyone that wants to have fun with it, go ahead.
Here you will find all the server files needed to run the server, it's not gonna be easy to setup, but it's better than nothing.

# Important Terms

-API: Service which handles operations like Logs/Player Data/Inventory backend
-DB: Database which holds all information needed to run all of this

# Notes

This doesn't bring all features asap had because some scripts were paid, hence not available to publicly release
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

You will need 2 things, a VPS which you can run your database (I highly recommend that over using your panel database)
Along this, you will need your game host as well, make sure your host allows you to run:

[Marketplace repository](https://github.com/ASAPGmod/marketplace)
-Place it wherever you want, don't forget to update [config details](https://github.com/ASAPGmod/marketplace/blob/main/config.js) with your database
Make sure to allow port 2052, you can by running **ufw allow 2052**

[Logs Repository](https://github.com/ASAPGmod/logs)
-The same as the marketplace, modify [config details](https://github.com/ASAPGmod/logs/blob/main/config.js) with your database
Make sure to allow port 2053, you can by running **ufw allow 2053**

[MySQL Driver config](https://github.com/ASAPGmod/driver/blob/main/lua/autorun/server/nebuladriver.lua)
-Set your credentials

Modify Marketplace API endpoint *(This script doesn't have an unique github repo, it's contained in the addons.7z)
asap_marketplace\lua\market\sh_meta.lua
Modify this: asapMarket.API = "http://145.239.205.161:2052" to the service URL your service it's placed, consider it's built into 2052 port

Modify Logs API endpoint *(Just like marketplace, this script doesn't have a repo, it's inside addons.7z)*
asap-log\lua\logs\api.lua
Modify this: asapLogs.API = "http://145.239.205.161:2053" to the service URL your service it's placed, consider it's built into 2053 port
asap-log\lua\logs\api.lua

Run many times server and client as you want, it needs to generate all DBs alone

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

Everything should just work, if it doesn't just ask support to my discord **el.gonzo**
No, i won't be fixing specific bugs or anything like that, but i will help you to get it launched or improve instructions over it

# Special thanks

To everyone at ASAPGaming members and to anyone that just liked the server enough to get something done from it
Fuck that stupid cunt that made me make it public due my stupidity, I won't mention you because you mean nothing to me, but it's a fact all this project might be helpful to anyone.

And special thanks to CodeBlue, the inventory and gobblegums were our stronger part of our gamemode, and I'm really proud to worked with someone like him the short time we could 🙏

❤
