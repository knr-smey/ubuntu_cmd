# Programming Languages

## Description

Language runtime and package manager notes for Node.js, Python, PHP, Java, Rust, Flutter, Composer, npm, pnpm, and version managers.

## Common Commands

```bash
node -v
npm -v
pnpm -v
python3 --version
pip3 --version
php -v
composer --version
java --version
rustc --version
cargo --version
flutter --version
```

## Examples

Install Node.js with Ubuntu packages:

```bash
sudo apt update
sudo apt install nodejs npm -y
```

Use NVM for Node.js version management:

```bash
nvm install 22
nvm use 22
nvm alias default 22
```

## Troubleshooting

- Wrong runtime version: check whether a version manager such as NVM, pyenv, SDKMAN, FVM, or rustup is active.
- Global package install fails: inspect permissions and prefer user-level version managers where possible.
- Command not found after install: reload the shell with `source ~/.bashrc` or open a new terminal.

## References

- [Node.js Documentation](https://nodejs.org/docs)
- [Python Documentation](https://docs.python.org/3/)
- [PHP Documentation](https://www.php.net/docs.php)
- [Rust Documentation](https://www.rust-lang.org/learn)
