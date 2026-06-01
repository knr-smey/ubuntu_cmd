# Ubuntu CMD

A collection of Ubuntu command notes and scripts.

## Features
- Linux commands
- Bash scripts
- Ubuntu tips

## Install Google Chrome

```bash
wget -q https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb && sudo apt install -y ./google-chrome-stable_current_amd64.deb
```
## Install VS Code

```bash
sudo apt update && sudo snap install code --classic
```
## Install Telegram

```bash
sudo apt update && sudo snap install telegram-desktop
```
## Install Open - VPN

```bash
sudo apt update && sudo apt install openvpn -y
```
## Connect to VPN
Place your `.ovpn` file in a folder, for example:

```bash
mkdir -p ~/vpn
```

Connect:
```bash
sudo openvpn --config ~/vpn/myvpn.ovpn
```

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

## Linux Folder & File Commands

```bash
# Create a folder
mkdir folder

# Create nested folders (parents automatically)
mkdir -p a/b/c

# Show files and folders
ls

# Show all files including hidden ones
ls -la

# Enter a folder
cd folder

# Go back one folder
cd ..

# Go to home folder
cd ~

# Go to root folder
cd /

# Show current folder path
pwd

# Create an empty file
touch file.txt

# Copy a file
cp file.txt backup.txt

# Move or rename a file
mv old.txt new.txt

# Move file to another folder
mv file.txt folder/

# Delete a file
rm file.txt

# Delete an empty folder
rmdir folder

# Delete a folder and its contents
rm -r folder

# Force delete folder and contents
rm -rf folder

# Search for a file
find . -name "file.txt"

# Show folder tree structure
tree

# Show disk usage of folders
du -sh *

# Show free disk space
df -h

# Show hidden files only
ls -d .*

# Create a symbolic link
ln -s target link

# Change file permissions
chmod 755 file.sh

# Change file owner
sudo chown user:user file.txt

# View file contents
cat file.txt

# View large file page by page
less file.txt

# View first 10 lines
head file.txt

# View last 10 lines
tail file.txt

# Monitor file changes live
tail -f logfile.log

# Create a zip archive
zip -r archive.zip folder/

# Extract zip archive
unzip archive.zip

# Create tar archive
tar -cvf archive.tar folder/

# Extract tar archive
tar -xvf archive.tar
```


## Author
KNR-Smey
