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

## Install Telegram

```bash
sudo apt update && sudo snap install telegram-desktop
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
