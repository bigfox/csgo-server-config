# CS:GO Config

## Server

1. Upload all files from `cfg` to `.../csgo/cfg/` folder on your server.
2. Upload all `mapcycle_....txt` files to `.../csgo/` folder on your server.

### Game Modes

|               | `game_mode 0` | `game_mode 1`    |
| ------------- | ------------- | ---------------- |
| `game_type 0` | Casual Mode   | Competitive Mode |
| `game_type 1` | Arms Race     | Demolition       |

#### Classic Casual

```plain
+exec server.cfg +game_type 0 +game_mode 0 +map de_dust2 +mapgroup mg_bomb +mapcyclefile mapcycle_casual.txt +sv_setsteamaccount [STEAM_LOGIN_TOKEN] -autoupdate
```

#### Classic Competitive

```plain
+exec server.cfg +game_type 0 +game_mode 1 +map de_dust2 +mapgroup mg_active +mapcyclefile mapcycle_competitive.txt +sv_setsteamaccount [STEAM_LOGIN_TOKEN] -autoupdate
```

#### Arms Race

```plain
+exec server.cfg +game_type 1 +game_mode 0 +map ar_shoots +mapgroup mg_armsrace +mapcyclefile mapcycle_armsrace.txt +sv_setsteamaccount [STEAM_LOGIN_TOKEN] -autoupdate
```

### SourceMod plugin

- [Documentation](https://wiki.alliedmods.net/Category:SourceMod_Documentation)
- [Adding Admins](https://wiki.alliedmods.net/Adding_Admins_(SourceMod)) to show admin menu

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