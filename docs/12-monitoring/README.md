# Monitoring

## Description

Monitoring notes for logs, metrics, alerts, uptime checks, dashboards, and observability tools.

## Common Commands

```bash
journalctl -xe
journalctl -u service_name
docker logs container_name
docker stats
top
htop
df -h
free -h
```

## Examples

Inspect service logs:

```bash
journalctl -u nginx --since "1 hour ago"
```

Watch Docker resource usage:

```bash
docker stats
```

## Troubleshooting

- Logs are missing: verify service name, log driver, permissions, and retention settings.
- Metrics are empty: check exporter status, scrape targets, firewall rules, and time range.
- Alerts are noisy: tune thresholds and add clear ownership or runbook links.

## References

- [Prometheus Documentation](https://prometheus.io/docs/)
- [Grafana Documentation](https://grafana.com/docs/)
- [systemd Journal Documentation](https://www.freedesktop.org/software/systemd/man/latest/journalctl.html)
