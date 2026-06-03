# Containers

## Description

Docker and Docker Compose notes for installing Docker, running containers, managing networks, building images, and running local development services.

## Common Commands

```bash
docker --version
docker ps
docker ps -a
docker images
docker logs container_name
docker exec -it container_name bash
docker compose up -d
docker compose down
```

## Examples

Install Docker from Ubuntu packages:

```bash
sudo apt update
sudo apt install docker.io -y
sudo systemctl enable --now docker
```

Create a Docker network:

```bash
docker network create dev-network
docker network ls
```

## Troubleshooting

- Permission denied when running Docker: add the user to the `docker` group, then log out and back in.
- Container exits immediately: inspect logs with `docker logs container_name`.
- Compose service cannot resolve another service: verify both services are on the same Compose network.

## References

- [Docker Documentation](https://docs.docker.com/)
- [Docker Compose Documentation](https://docs.docker.com/compose/)
