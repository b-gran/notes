# Docker

## Deleting Compose volumes

Compose volumes are listed alongside the rest of your Docker volumes:
```bash
docker volume ls
```

To properly remove them, however, they need to be removed using `docker-compose`.

The `docker-compose down` command is able to remove volumes. Unfortunately, you can't remove the volumes of a specific container. You can only remove *all* the volumes specified in a `docker-compose.yml`.

To remove *all* volumes for a Compose config, do the following:
```bash
docker-compose down --volumes
```
