# Developer Tools

## Description

Setup and command notes for Git, VS Code, browsers, terminals, pgAdmin, and other local development tools.

## Common Commands

```bash
git status
git log --oneline --decorate --graph
code --version
code .
google-chrome --version
```

## Examples

Install VS Code with Snap:

```bash
sudo snap install code --classic
```

Install Google Chrome:

```bash
wget -q https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install -y ./google-chrome-stable_current_amd64.deb
```

## Troubleshooting

- VS Code command not found: confirm the `code` command is installed and available in `PATH`.
- Git identity missing: configure `git config --global user.name` and `git config --global user.email`.
- Browser package install fails: run `sudo apt update` and check the downloaded `.deb` path.

## References

- [Git Documentation](https://git-scm.com/doc)
- [Visual Studio Code Documentation](https://code.visualstudio.com/docs)
