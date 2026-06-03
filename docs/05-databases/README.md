# Databases

## Description

Database setup and command notes for PostgreSQL, MySQL, MongoDB, Redis, pgAdmin, phpMyAdmin, Mongo Express, and Redis Insight.

## Common Commands

```bash
psql --version
mysql --version
mongosh --version
redis-cli --version
docker ps
docker logs container_name
```

## Examples

Run PostgreSQL with Docker:

```bash
docker run -d \
  --name postgres \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=root \
  -e POSTGRES_DB=appdb \
  -p 5432:5432 \
  postgres:17
```

Connect to PostgreSQL:

```bash
docker exec -it postgres psql -U postgres
```

## Troubleshooting

- Port already in use: check running services with `sudo ss -tulpn`.
- Cannot connect from admin UI: verify container network, hostname, port, username, and password.
- Data disappeared after container removal: use named volumes for persistent database data.

## References

- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
- [MySQL Documentation](https://dev.mysql.com/doc/)
- [MongoDB Documentation](https://www.mongodb.com/docs/)
- [Redis Documentation](https://redis.io/docs/latest/)
