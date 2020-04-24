# CS:GO Config

## Server

1. Set server name and passwords in `cfg/server.cfg`
2. Upload folders `cfg` and `addons` to `.../csgo/` folder on your server.

### Game Modes

|               | `game_mode 0` | `game_mode 1`    |
| ------------- | ------------- | ---------------- |
| `game_type 0` | Casual Mode   | Competitive Mode |
| `game_type 1` | Arms Race     | Demolition       |

### Startup options

#### Classic Casual

```plain
+exec server.cfg +game_type 0 +game_mode 0 +map de_dust2 +mapgroup mg_bomb +sv_setsteamaccount [STEAM_LOGIN_TOKEN] -autoupdate
```

#### Classic Competitive

```plain
+exec server.cfg +game_type 0 +game_mode 1 +map de_dust2 +mapgroup mg_active +sv_setsteamaccount [STEAM_LOGIN_TOKEN] -autoupdate
```

#### Arms Race

```plain
+exec server.cfg +game_type 1 +game_mode 0 +map ar_shoots +mapgroup mg_armsrace +sv_setsteamaccount [STEAM_LOGIN_TOKEN] -autoupdate
```

### SourceMod plugin

- [Documentation](https://wiki.alliedmods.net/Category:SourceMod_Documentation)
- [Adding Admins](https://wiki.alliedmods.net/Adding_Admins_(SourceMod)) to show admin menu

To disable `nextmap` plugin (breaks native map voting) move `csgo/addons/sourcemod/plugins/nextmap.smx` to `csgo/addons/sourcemod/plugins/disabled/` folder.

## Client

### Setup RCON

```plain
rcon_address [host/ip:port]
rcon_password [password]
```

### Commands

| Command | Description |
| --- | --- |
| `rcon bot_kick` | Kick all bots |
| `rcon bot_add` | Add random bot |
| `rcon bot_add_ct` | Add counter-terrorist bot |
| `rcon bot_add_t` | Add terrorist bot |
| `rcon changelevel [map_code]` | Change map to [map_code] (e.g. de_dust2, de_inferno ...) |

### Show SourceMod Admin Menu

Bind key F11 to command `sm_admin` (see [How to: Scripting, Binds and Configs](https://steamcommunity.com/sharedfiles/filedetails/?id=314801693))