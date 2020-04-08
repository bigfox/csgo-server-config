# CS:GO Server Config

Upload `server.cfg` and `gamemode_competitive_server.cfg` to `.../csgo/cfg/` folder on your server

## Setup RCON

```bash
rcon_address [host/ip:port]
rcon_password [password]
```

## Bots commands

### Kick all bots

```bash
rcon bot_kick
```

### Add random bot

```bash
rcon bot_add
```

### Add counter-terrorist bot

```bash
rcon bot_add_ct
```

### Add terrorist bot

```bash
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
