# CS:GO Config

## Server

1. Set server name and passwords in `cfg/server.cfg`
2. Upload file `gamemodes_server.txt` and folders `cfg` and `addons` to `.../csgo/` folder on your server.

### Game Modes

|                     | `game_type` | `game_mode` | `map`        | `mapgroup`      |
|---------------------|-------------|-------------|--------------|-----------------|
| Classic Casual      | `0`         | `0`         |              |                 |
| Classic Competitive | `0`         | `1`         | `de_dust2`   | `mg_active`     |
| Arms Race           | `1`         | `0`         | `ar_shoots`  | `mg_armsrace`   |
| Demolition          | `1`         | `1`         | `de_lake`    | `mg_demolition` |
| Deathmatch          | `1`         | `2`         | `de_dust2`   | `mg_deathmatch` |
| Wingman (2v2)       | `0`         | `2`         | `de_vertigo` | `mg_wingman`    |

### Startup options

```plain
+exec server.cfg +game_type [GAME_TYPE] +game_mode [GAME_MODE] +map [MAP] +mapgroup [MAPGROUP] +sv_setsteamaccount [STEAM_LOGIN_TOKEN] -autoupdate
```

### SourceMod plugin

- [Documentation](https://wiki.alliedmods.net/Category:SourceMod_Documentation)
- [Adding Admins](https://wiki.alliedmods.net/Adding_Admins_(SourceMod)) to show admin menu

To disable `nextmap` plugin (breaks native map voting) move `csgo/addons/sourcemod/plugins/nextmap.smx` to `csgo/addons/sourcemod/plugins/disabled/` folder.

## Client

### Setup RCON

1. Set RCON password

   ```plain
   rcon_password [YOUR_SERVER_RCON_PASSWORD]
   ```

2. Use `rcon` command before all commands

### Commands

| Command                  | Description                                         |
|--------------------------|-----------------------------------------------------|
| `rcon bot_kick`          | Kick all bots                                       |
| `rcon bot_add`           | Add random bot                                      |
| `rcon bot_add_ct`        | Add counter-terrorist bot                           |
| `rcon bot_add_t`         | Add terrorist bot                                   |
| `rcon changelevel [MAP]` | Change map to [MAP] (e.g. de_dust2, de_inferno ...) |

### Show SourceMod Admin Menu

Bind key F11 to command `sm_admin` (see [How to: Scripting, Binds and Configs](https://steamcommunity.com/sharedfiles/filedetails/?id=314801693))