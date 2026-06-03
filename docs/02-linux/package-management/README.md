# Package Management

## Description

Ubuntu package management commands for updating repositories, installing packages, removing packages, searching software, managing `.deb` files with `dpkg`, managing Snap packages, and cleaning unused dependencies.

## Common Commands

```bash
sudo apt update
sudo apt upgrade -y
sudo apt full-upgrade -y
apt search package_name
apt show package_name
sudo apt install package_name -y
sudo apt remove package_name -y
sudo apt purge package_name -y
sudo apt autoremove -y
sudo apt clean
sudo apt autoclean
dpkg --version
dpkg -l
dpkg -l | grep package_name
dpkg -s package_name
sudo dpkg -i package_file.deb
sudo dpkg -r package_name
snap list
sudo snap install package_name
sudo snap remove package_name
```

## Examples

Install common developer packages:

```bash
sudo apt update
sudo apt install curl wget git unzip ca-certificates gnupg -y
```

Search for a package:

```bash
apt search postgresql
```

Show package details:

```bash
apt show docker.io
```

Remove a package but keep config files:

```bash
sudo apt remove package_name -y
```

Remove a package and its config files:

```bash
sudo apt purge package_name -y
sudo apt autoremove -y
```

Install VS Code with Snap:

```bash
sudo snap install code --classic
```

Install a downloaded `.deb` package with `dpkg`:

```bash
sudo dpkg -i package_file.deb
sudo apt --fix-broken install
```

List installed packages with `dpkg`:

```bash
dpkg -l
dpkg -l | grep docker
```

Show package status:

```bash
dpkg -s docker.io
```

Remove a package with `dpkg`:

```bash
sudo dpkg -r package_name
```

## APT vs dpkg

Use `apt` for normal package installation because it downloads packages and resolves dependencies automatically.

Use `dpkg` when you already have a local `.deb` file or need low-level package information. `dpkg` does not automatically download missing dependencies, so after installing a `.deb` file you may need:

```bash
sudo apt --fix-broken install
```

## Troubleshooting

- `Unable to locate package`: run `sudo apt update`, then verify the package name.
- `Could not get lock`: another package process is running. Wait for it to finish before trying again.
- Broken packages: run `sudo apt --fix-broken install`.
- `dpkg: dependency problems`: run `sudo apt --fix-broken install`.
- Repository key errors: verify the official repository setup instructions and keyring path.
- Snap command not found: install Snap with `sudo apt install snapd -y`.

## References

- [Ubuntu Packages](https://packages.ubuntu.com/)
- [APT User Guide](https://manpages.ubuntu.com/manpages/latest/man8/apt.8.html)
- [dpkg Manual Page](https://manpages.ubuntu.com/manpages/latest/man1/dpkg.1.html)
- [Snap Documentation](https://snapcraft.io/docs)
