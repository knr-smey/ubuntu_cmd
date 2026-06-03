# Ubuntu

## Description

Ubuntu-specific commands for system setup, desktop configuration, package installation, language settings, software management, and system maintenance.

---

## Common Commands

```bash
lsb_release -a
cat /etc/os-release
hostnamectl
sudo apt update
sudo apt upgrade -y
sudo apt autoremove -y
sudo reboot
sudo shutdown now
df -h
free -h
top
htop
```

---

## Examples

### Check Ubuntu Version

```bash
lsb_release -a
```

### Check System Information

```bash
hostnamectl
```

### Update Ubuntu

```bash
sudo apt update
sudo apt upgrade -y
```

### Remove Unused Packages

```bash
sudo apt autoremove -y
sudo apt autoclean
```

### Install Common Utilities

```bash
sudo apt install curl wget git unzip tree htop -y
```

### Check Disk Usage

```bash
df -h
```

### Check Memory Usage

```bash
free -h
```

### Check Running Processes

```bash
top
```

### Install Htop

```bash
sudo apt install htop -y
htop
```

### Reboot System

```bash
sudo reboot
```

### Shutdown System

```bash
sudo shutdown now
```

### Change Hostname

```bash
sudo hostnamectl set-hostname new-hostname
```

### Verify Hostname

```bash
hostnamectl
```

### Open Ubuntu Settings

```bash
gnome-control-center
```

### Open Region & Language Settings

```bash
gnome-control-center region
```

### Check Locale

```bash
locale
```

### Check Language Configuration

```bash
localectl status
```

---

## Ubuntu Desktop

### Open Network Settings

```bash
gnome-control-center network
```

### Open Display Settings

```bash
gnome-control-center display
```

### Open Power Settings

```bash
gnome-control-center power
```

### Open Bluetooth Settings

```bash
gnome-control-center bluetooth
```

---

## Troubleshooting

### Command Not Found

Install the package containing the command:

```bash
sudo apt install package_name
```

### Package Database Issues

```bash
sudo apt --fix-broken install
```

### Low Disk Space

Check large directories:

```bash
du -sh *
df -h
```

### High Memory Usage

```bash
free -h
top
htop
```

### System Logs

```bash
journalctl -xe
```

### Check Service Status

```bash
systemctl status service_name
```

---

## References

* Ubuntu Documentation
* Ubuntu Community Help Wiki
* Ubuntu Desktop Guide
* GNOME Documentation
