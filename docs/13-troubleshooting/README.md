# Troubleshooting

## Description

Central troubleshooting notes for common workstation, application, Docker, network, database, and deployment problems.

## Common Commands

```bash
uname -a
lsb_release -a
sudo ss -tulpn
ping example.com
curl -I https://example.com
df -h
free -h
docker ps -a
docker logs container_name
```

## Examples

Check whether a port is being used:

```bash
sudo ss -tulpn
```

Check HTTP response headers:

```bash
curl -I https://example.com
```

## Troubleshooting

- Start with the smallest failing command and record the exact error.
- Check logs before changing configuration.
- Verify versions, environment variables, ports, permissions, and network access.
- After a fix, document the root cause and the final command that solved it.

## References

- [Ubuntu Server Troubleshooting](https://documentation.ubuntu.com/server/)
- [Docker Troubleshooting](https://docs.docker.com/engine/daemon/troubleshoot/)
