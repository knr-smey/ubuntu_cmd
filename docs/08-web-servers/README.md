# Web Servers

## Description

Web server notes for Nginx, Apache, reverse proxies, virtual hosts, TLS, redirects, and local development routing.

## Common Commands

```bash
nginx -v
sudo nginx -t
sudo systemctl status nginx
sudo systemctl reload nginx
apache2 -v
sudo systemctl status apache2
```

## Examples

Run Nginx with Docker:

```bash
docker run -d \
  --name nginx \
  -p 80:80 \
  nginx
```

Test Nginx configuration:

```bash
sudo nginx -t
```

## Troubleshooting

- Port 80 already in use: check listeners with `sudo ss -tulpn`.
- Nginx reload fails: run `sudo nginx -t` before reloading.
- Site not reachable: verify firewall rules, DNS, proxy config, and upstream application status.

## References

- [Nginx Documentation](https://nginx.org/en/docs/)
- [Apache HTTP Server Documentation](https://httpd.apache.org/docs/)
