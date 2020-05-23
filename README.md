Forked from https://github.com/jimtouz/counter-strike-docker

Updated to work with Steam Guard Code and docker-compose.

# Docker image for Counter Strike 1.6 Dedicated Server

## Start the server

### Minimum properties setup

```bash
docker-compose up -d
```
#### Propetries

| Name | Description | Default Value |
| --- | --- | --- |
| `STEAM_USER` | Steam user name to authenticate dedicated server | None |
| `STEAM_PASSWORD` | Steam password for auth user | None |
| `STEAM_GUARD_CODE` | Will be received after first run of `docker-compose build` | None |
| `MAXPLAYERS` | The maximum number of players | `32` |
| `START_MAP` | The initial map | `de_dust2` |
| `SERVER_NAME` | The server name | `Counter-Strike 1.6 Server` |
| `START_MONEY` | The initial money | `800` |
| `BUY_TIME` | The allowed time to buy items in each round (*minutes*) | `0.25` |
| `FRIENDLY_FIRE` | Enable or disable the friendly fire. (*off: 0, on: 1*) | `1` |
| `SERVER_PASSWORD` | The server password. (*Empty for no server password*) | None |
| `RCON_PASSWORD` | The rcon password. (*Empty for no rcon password*) | None |
| `RESTART_ON_FAIL` | *TBD* | *TBD* |
| `ADMIN_STEAM` | *TBD - amx mod related*| *TBD* |

## Stop the server

```bash
docker-compose up -d
```

## Remove the server

```bash
docker-compose rm
```

# Attributions

This project is based on [counter-strike-docker](https://github.com/artem-panchenko/counter-strike-docker), developed by [Artem Panchenko](https://github.com/artem-panchenko).

## Changes from original project

* Changed the name of the build.
* Added new maps.
* Added new parameters in run script.
