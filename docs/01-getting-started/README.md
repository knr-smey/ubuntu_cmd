# Getting Started

## Description

This section explains how to use and extend this personal DevOps and Full Stack Developer command handbook.

## Common Commands

```bash
find docs -maxdepth 2 -type f | sort
git status
git add README.md docs/
git commit -m "Organize documentation handbook"
```

## Examples

Create a new topic page:

```bash
mkdir -p docs/06-containers/docker
touch docs/06-containers/docker/install-docker.md
```

Recommended topic filename style:

```text
install-docker.md
docker-networking.md
postgresql-backup-restore.md
laravel-local-setup.md
```

## Troubleshooting

- If a topic becomes too large, split it into smaller files inside the same category folder.
- If a command is OS-specific, mention the tested Ubuntu version or environment.
- If a command can remove files, containers, images, or data, add a warning before it.

## References

- [GitHub Docs: Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github)
- [GitHub Docs: About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
