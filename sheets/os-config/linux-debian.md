# Linux - Debian commands

Here are some recipes that might be useful for a Debian configuration on your desktop.


## Package manager

```bash
# update repositories :
sudo apt update
sudo apt upgrade
sudo apt install

# install a package :
sudo apt install <pkg>

# remove a package :
sudo apt remove <pkg>

# search a package (distant) :
apt search <pkg>

# search a package (local) :
dpkg -l | grep -i <pkg>
```

## Fresh install steps

### Basic programs
```bash
# network
sudo apt install curl
sudo apt install falkon
sudo apt install wireshark-qt

# system
sudo apt install vim htop ncdu
sudo apt install neofetch
```

### Set the locale timezone
```bash
dpkg-reconfigure tzdata
```

### Add an icon for an application (ex: Postman)
```bash
cat > ~/.local/share/applications/Postman.desktop <<EOL
[Desktop Entry]
Type=Application
Name=Postman
Exec=/home/myuser/.local/bin/postman
Icon=/home/myuser/dev/progs/Postman/app/resources/app/assets/icon.png
Categories=Development;
Encoding=UTF-8
Terminal=false
EOL
```

### Handle zip/tar archives

#### Create an archive
```bash
tar -czvf file.tar.gz directory

# or
zip -r file.zip directory
```

#### Extract an archive
```bash
tar -zxf file.tar.gz

# or
tar -xf file.tar.xz

# or
unzip file.zip

# or, for a debian package
ar x dpkg_1.17.23_amd64.deb
```

### Useful links
* [Debian on the Desktop](https://www.debian.org/devel/debian-desktop/index.en.html)
* [DebianDesktopHowTo](https://wiki.debian.org/DebianDesktopHowTo)
* [How to install and use Debian backports](https://linuxconfig.org/how-to-install-and-use-debian-backports)
