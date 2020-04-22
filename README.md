# CS:GO Server Config

Upload `server.cfg` and `gamemode_competitive_server.cfg` to `.../csgo/cfg/` folder on your server

## Game Modes

### Classic Casual

```plain
+exec server.cfg +game_type 0 +game_mode 0 +map de_dust2 +mapgroup mg_bomb +sv_setsteamaccount [STEAM_LOGIN_TOKEN] -autoupdate
```

### Classic Competitive

```plain
+exec server.cfg +game_type 0 +game_mode 1 +map de_dust2 +mapgroup mg_active +sv_setsteamaccount [STEAM_LOGIN_TOKEN] -autoupdate
```

### Arms Race

```plain
+exec server.cfg +game_type 1 +game_mode 0 +map ar_shoots +mapgroup mg_armsrace +sv_setsteamaccount [STEAM_LOGIN_TOKEN] -autoupdate
```

## Setup RCON

```plain
rcon_address [host/ip:port]
rcon_password [password]
```

## Bot commands

### Kick all bots

```plain
rcon bot_kick
```

### Add random bot

```plain
rcon bot_add
```

### Add counter-terrorist bot

```plain
rcon bot_add_ct
```

### Add terrorist bot

```plain
rcon bot_add_t
```

## Change map

```plain
rcon changelevel [map_code]
rcon changelevel de_dust2
rcon changelevel de_inferno
rcon changelevel cs_italy
rcon changelevel cs_office
```
