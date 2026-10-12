# calibre-swarm

E-book management server.

## Stack

- **Host**: ore-dock-110-1
- **Stack**: `calibre-swarm`
- **Image**: lscr.io/linuxserver/calibre:latest
- **Config**: named volumes `calibre-swarm.config`, `calibre-swarm.db`

## Ports

| Port | Published | Protocol |
|------|----------|----------|
| 8080 | 8080 | TCP |
| 8082 | 8082 | TCP |
| 8181 | 8181 | TCP |

## Deploy

```bash
ssh ore-dock-110-1
cd /data/compose/calibre-swarm
set -a && source .env && docker stack deploy -c docker-compose.yml --with-registry-auth calibre-swarm && set +a
```
