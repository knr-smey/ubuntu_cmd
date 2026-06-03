# Personal DevOps and Full Stack Command Handbook

A practical knowledge base for Ubuntu, Linux commands, Docker, Laravel, PostgreSQL, Git, VS Code, VPN, and daily developer operations.

This repository is organized as a scalable handbook: each category has its own folder, a category `README.md`, and topic subfolders for deeper notes, examples, scripts, and troubleshooting.

## Table of Contents

- [Getting Started](docs/01-getting-started/README.md)
- [Linux and Ubuntu](docs/02-linux/README.md)
- [Developer Tools](docs/03-developer-tools/README.md)
- [Programming Languages](docs/04-programming-languages/README.md)
- [Databases](docs/05-databases/README.md)
- [Containers](docs/06-containers/README.md)
- [Frameworks](docs/07-frameworks/README.md)
- [Web Servers](docs/08-web-servers/README.md)
- [DevOps](docs/09-devops/README.md)
- [Cloud](docs/10-cloud/README.md)
- [Security](docs/11-security/README.md)
- [Monitoring](docs/12-monitoring/README.md)
- [Troubleshooting](docs/13-troubleshooting/README.md)
- [References](docs/99-references/README.md)

## Documentation Structure

```text
docs/
├── 01-getting-started/
├── 02-linux/
│   ├── ubuntu/
│   ├── package-management/
│   ├── commands/
│   ├── networking/
│   └── security/
├── 03-developer-tools/
│   ├── git/
│   ├── vscode/
│   ├── browsers/
│   └── terminals/
├── 04-programming-languages/
│   ├── nodejs/
│   ├── python/
│   ├── php/
│   ├── java/
│   ├── rust/
│   └── flutter/
├── 05-databases/
│   ├── postgresql/
│   ├── mysql/
│   ├── mongodb/
│   └── redis/
├── 06-containers/
│   ├── docker/
│   ├── docker-compose/
│   └── container-images/
├── 07-frameworks/
│   ├── laravel/
│   └── frontend/
├── 08-web-servers/
│   ├── nginx/
│   └── apache/
├── 09-devops/
│   ├── ci-cd/
│   ├── kubernetes/
│   └── infrastructure-as-code/
├── 10-cloud/
│   ├── aws/
│   ├── azure/
│   └── gcp/
├── 11-security/
│   ├── vpn/
│   ├── secrets/
│   └── hardening/
├── 12-monitoring/
│   ├── logging/
│   ├── metrics/
│   └── alerting/
├── 13-troubleshooting/
└── 99-references/
```

## Writing Format

Use this format for every topic page:

```markdown
# Topic Name

## Description

Explain what the tool, command, or workflow is used for.

## Common Commands

List the most frequently used commands.

## Examples

Show realistic copy-ready usage examples.

## Troubleshooting

Document common errors, checks, and fixes.

## References

Link to official documentation and trusted sources.
```

## Best Practices

- Keep one topic per file when a category grows.
- Prefer official documentation in the `References` section.
- Use fenced code blocks with language labels such as `bash`, `yaml`, `sql`, or `text`.
- Keep commands copy-ready and add warnings before destructive operations.
- Avoid storing secrets, tokens, private keys, or production passwords.
- Add troubleshooting notes when a command has common failure cases.

## Author

KNR-Smey
