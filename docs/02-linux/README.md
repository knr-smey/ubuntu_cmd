# Linux and Ubuntu

## Description

Ubuntu and Linux command notes for system setup, package management, file operations, networking, services, and basic security.

## Topics

- [Ubuntu](ubuntu/)
- [Package Management](package-management/)
- [Commands](commands/)
- [Networking](networking/)
- [Security](security/)

## Common Commands

```bash
sudo apt update
sudo apt upgrade -y
apt search package_name
sudo apt install package_name -y
sudo apt remove package_name -y
ls -lah
pwd
cd /path/to/project
systemctl status service_name
ip addr
df -h
free -h
```

## Examples

Install common Ubuntu packages:

```bash
sudo apt update
sudo apt install curl wget ca-certificates gnupg unzip -y
```

Check a service:

```bash
sudo systemctl status ssh
```

## Troubleshooting

- `Unable to locate package`: run `sudo apt update` and verify the package name.
- Permission denied: check whether the command requires `sudo` or file ownership changes.
- Service not starting: inspect `systemctl status service_name` and `journalctl -u service_name`.

## References

- [Ubuntu Documentation](https://help.ubuntu.com/)
- [Ubuntu Packages](https://packages.ubuntu.com/)
- [systemd Manual Pages](https://www.freedesktop.org/software/systemd/man/latest/)
