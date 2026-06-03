# Security

## Description

Security notes for VPN, secrets management, local hardening, antivirus scanning, SSH keys, access control, and safe developer workstation practices.

## Common Commands

```bash
ssh -V
ssh-keygen -t ed25519 -C "your-email@example.com"
sudo ufw status
sudo ufw enable
clamscan --version
sudo freshclam
```

## Examples

Generate an SSH key:

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

Scan the home directory with ClamAV:

```bash
clamscan -r ~/ --bell -i
```

## Troubleshooting

- SSH login fails: check file permissions, public key placement, username, host, and firewall rules.
- VPN connects but traffic fails: verify DNS, routes, split tunnel settings, and firewall rules.
- ClamAV database update fails: check network access and whether another update process is running.

## References

- [OpenSSH Manual Pages](https://www.openssh.com/manual.html)
- [Ubuntu Security Documentation](https://ubuntu.com/security)
- [ClamAV Documentation](https://docs.clamav.net/)
