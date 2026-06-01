# Ubuntu CMD 🚀

A collection of Ubuntu command notes and scripts.

## 📋 Table of Contents

* Browsers
* Development Tools
* VPN & Network
* Docker & Containers
* Web Servers
* File & Folder Commands
* System Commands

---

# 🌐 Browsers

## Install Google Chrome

```bash
wget -q https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb && sudo apt install -y ./google-chrome-stable_current_amd64.deb
```

---

# 💻 Development Tools

## Install VS Code

```bash
sudo apt update && sudo snap install code --classic
```

### Check Version

```bash
code --version
```

### Remove VS Code

```bash
sudo snap remove code
```

---

## Install Telegram

```bash
sudo apt update && sudo snap install telegram-desktop
```

### Launch Telegram

```bash
telegram-desktop
```

### Remove Telegram

```bash
sudo snap remove telegram-desktop
```

---

## 🛡️ Install ClamAV

### Install ClamAV

```bash
sudo apt update && sudo apt install clamav clamav-daemon -y
```

### Check Version

```bash
clamscan --version
```

### Update Virus Database

```bash
sudo freshclam
```

### Scan Home Directory

```bash
clamscan -r ~/ --bell -i
```

### Scan Entire System

```bash
sudo clamscan -r / --bell -i
```

### Start ClamAV Service

```bash
sudo systemctl start clamav-daemon
```

### Enable ClamAV on Boot

```bash
sudo systemctl enable clamav-daemon
```

### Check Service Status

```bash
sudo systemctl status clamav-daemon
```

### Remove ClamAV

```bash
sudo apt remove clamav clamav-daemon -y
sudo apt autoremove -y
```
---

# 🚀 Programming Languages & Package Managers

## Install Node.js + npm

```bash
sudo apt update && sudo apt install nodejs npm -y
```

### Check Version

```bash
node -v
npm -v
```


## Install PNPM

```bash
sudo npm install -g pnpm
```

### Check Version

```bash
pnpm -v
```

---

## Install Python + pip

```bash
sudo apt update && sudo apt install python3 python3-pip -y
```

### Check Version

```bash
python3 --version
pip3 --version
```

---

# 🔄 Version Management

## Node.js (NVM)

Install NVM:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
source ~/.bashrc
```

Install Versions:

```bash
nvm install 20
nvm install 22
```

List Versions:

```bash
nvm ls
```

Switch Version:

```bash
nvm use 20
nvm use 22
```

Default Version:

```bash
nvm alias default 22
```

---

## Python (Pyenv)

Install Versions:

```bash
pyenv install 3.11
pyenv install 3.12
```

List Versions:

```bash
pyenv versions
```

Global Version:

```bash
pyenv global 3.12
```

Project Version:

```bash
pyenv local 3.11
```

---

## PHP

Show Installed Versions:

```bash
update-alternatives --list php
```

Switch Version:

```bash
sudo update-alternatives --config php
```

Check Version:

```bash
php -v
```

---

## Flutter (FVM)

Install FVM:

```bash
dart pub global activate fvm
```

Install Flutter Version:

```bash
fvm install 3.32.0
```

Use Version:

```bash
fvm use 3.32.0
```

List Versions:

```bash
fvm list
```

---

## Java (SDKMAN)

Install SDKMAN:

```bash
curl -s "https://get.sdkman.io" | bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
```

Install Versions:

```bash
sdk install java 21-tem
sdk install java 17-tem
```

Switch Version:

```bash
sdk use java 21-tem
```

Default Version:

```bash
sdk default java 21-tem
```

---

## Rust (Rustup)

Install Toolchain:

```bash
rustup install stable
rustup install nightly
```

List Toolchains:

```bash
rustup toolchain list
```

Switch Version:

```bash
rustup default stable
rustup default nightly
```

---

## Docker (Version Isolation)

Instead of switching versions globally, run the version you need:

### Node.js

```bash
docker run --rm node:20 node -v
docker run --rm node:22 node -v
```

### Python

```bash
docker run --rm python:3.11 python --version
docker run --rm python:3.12 python --version
```

### PHP

```bash
docker run --rm php:8.1 php -v
docker run --rm php:8.4 php -v
```

### Composer

```bash
docker run --rm composer --version
```

### MySQL

```bash
docker run -d --name mysql8 -e MYSQL_ROOT_PASSWORD=root mysql:8
```

### PostgreSQL

```bash
docker run -d --name postgres17 -e POSTGRES_PASSWORD=root postgres:17
```

---

## Recommended Setup

```text
Git        -> Ubuntu
VS Code    -> Ubuntu
Chrome     -> Ubuntu
Docker     -> Ubuntu

Node.js    -> NVM
Python     -> Pyenv
PHP        -> Docker or update-alternatives
Flutter    -> FVM
Java       -> SDKMAN
Rust       -> Rustup

MySQL      -> Docker
PostgreSQL -> Docker
MongoDB    -> Docker
Redis      -> Docker
```
---

## Install PHP

```bash
sudo apt update && sudo apt install php -y
```

### Check Version

```bash
php -v
```

---

## Install Composer

```bash
sudo apt update && sudo apt install composer -y
```
---
### Check Version

```bash
composer --version
```

---

## Install Java (OpenJDK)

```bash
sudo apt update && sudo apt install openjdk-21-jdk -y
```

### Check Version

```bash
java --version
javac --version
```

---

## Install Rust

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### Check Version

```bash
rustc --version
cargo --version
```

---

## Install Flutter

```bash
sudo snap install flutter --classic
```

### Check Installation

```bash
flutter doctor
```
---

# 🔒 VPN & Network

## Install OpenVPN

```bash
sudo apt update && sudo apt install openvpn -y
```

## Create VPN Folder

```bash
mkdir -p ~/vpn
```

## Connect VPN

```bash
sudo openvpn --config ~/vpn/myvpn.ovpn
```

---

# 🐳 Docker & Containers

## Install Docker

```bash
sudo apt update && sudo apt install docker.io -y
```

## Start Docker

```bash
sudo systemctl start docker
```

## Enable Docker on Boot

```bash
sudo systemctl enable docker
```

## Check Docker Version

```bash
docker --version
```

## Test Docker

```bash
sudo docker run hello-world
```

## Run Docker Without sudo

```bash
sudo usermod -aG docker $USER
newgrp docker
```

---

# 🌍 Web Servers

## Install Apache, PHP, MySQL

```bash
sudo apt update
sudo apt install apache2 php mysql-server -y
```

## Start Services

```bash
sudo systemctl start apache2
sudo systemctl start mysql
```

## Enable on Boot

```bash
sudo systemctl enable apache2
sudo systemctl enable mysql
```

## Check Status

```bash
sudo systemctl status apache2
sudo systemctl status mysql
```

## Remove Apache, PHP, MySQL

```bash
sudo apt remove apache2 php mysql-server -y
sudo apt autoremove -y
```

---

# 📁 File & Folder Commands

```bash
# Show current directory
pwd

# List files and folders
ls

# List all files including hidden
ls -la

# List files with sizes
ls -lh

# Enter folder
cd folder

# Go back one level
cd ..

# Go to home directory
cd ~

# Go to root directory
cd /

# Create folder
mkdir folder

# Create nested folders
mkdir -p folder/subfolder

# Remove empty folder
rmdir folder

# Remove folder and contents
rm -r folder

# Force remove folder and contents
rm -rf folder

# Create file
touch file.txt

# View file contents
cat file.txt

# Read file page by page
less file.txt

# First 10 lines
head file.txt

# Last 10 lines
tail file.txt

# Monitor file changes
tail -f file.log

# Copy file
cp file.txt backup.txt

# Copy folder
cp -r folder backup_folder

# Move file
mv file.txt folder/

# Rename file
mv old.txt new.txt

# Delete file
rm file.txt

# Search for file
find . -name "file.txt"

# Search for folder
find . -type d -name "folder"

# Search text in file
grep "text" file.txt

# Search text recursively
grep -r "text" .

# Show directory tree
tree

# Show folder size
du -sh folder

# Show all folder sizes
du -sh *

# Show free disk space
df -h

# Show mounted drives
mount

# Create symbolic link
ln -s target link

# Change permissions
chmod 755 file.sh

# Make file executable
chmod +x script.sh

# Change owner
sudo chown user:user file.txt

# Show file information
stat file.txt

# Compare files
diff file1.txt file2.txt

# Count lines, words, characters
wc file.txt

# Sort file content
sort file.txt

# Remove duplicate lines
uniq file.txt

# Create ZIP archive
zip -r archive.zip folder/

# Extract ZIP archive
unzip archive.zip

# Create TAR archive
tar -cvf archive.tar folder/

# Extract TAR archive
tar -xvf archive.tar

# Create TAR.GZ archive
tar -czvf archive.tar.gz folder/

# Extract TAR.GZ archive
tar -xzvf archive.tar.gz

# Create TAR.XZ archive
tar -cJvf archive.tar.xz folder/

# Extract TAR.XZ archive
tar -xJvf archive.tar.xz
```
---

## Package Management (dpkg)

### Install .deb Package

```bash
sudo dpkg -i package.deb
```

### Remove Package

```bash
sudo dpkg -r package_name
```

### Remove Package + Config Files

```bash
sudo dpkg -P package_name
```

### List Installed Packages

```bash
dpkg -l
```

### Search Installed Package

```bash
dpkg -l | grep package_name
```

### Show Package Information

```bash
dpkg -s package_name
```

### List Files Installed by Package

```bash
dpkg -L package_name
```

### Find Which Package Owns a File

```bash
dpkg -S /usr/bin/code
```

### Fix Missing Dependencies

```bash
sudo apt --fix-broken install
```

---

# ⚙️ System Commands

## Update Packages

```bash
sudo apt update
```

## Upgrade Packages

```bash
sudo apt upgrade -y
```

## Remove Unused Packages

```bash
sudo apt autoremove -y
```

## Show Ubuntu Version

```bash
lsb_release -a
```

## Show Kernel Version

```bash
uname -r
```

## Show CPU Information

```bash
lscpu
```

## Show Memory Usage

```bash
free -h
```

## Show Disk Usage

```bash
df -h
```

## Show Running Processes

```bash
ps aux
```

## Monitor System

```bash
htop
```

## Reboot System

```bash
sudo reboot
```

## Shutdown System

```bash
sudo shutdown now
```
---

# 👨‍💻 Author

**KNR-Smey**
