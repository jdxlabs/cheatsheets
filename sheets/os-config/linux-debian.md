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

### Update password
```bash
# as the user who wants to change the password
passwd
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

### UI Look

```bash
# Install Gnome Tweaks and Papirus icon theme
sudo apt install gnome-tweaks
sudo apt install papirus-icon-theme

# Install Dash to Dock extension
sudo apt install gnome-shell-extension-dash-to-dock

# Install a pack of preinstalled extensions
sudo apt install gnome-shell-extensions
```

To make the magic happen, you need to go to your Settings:
- Go to Tweaks - Appearance
- Icons tab: Choose Papirus-Dark.
- To show again maximize and minimize buttons: go to Windows - Titlebar Buttons and enable "Maximize" and "Minimize".

To improve the look:
- Go to Extensions
- Enable "Dash to Dock" and configure it to display only icons, and to hide the dock when windows are maximized.

By the way, you can find the list of all the extensions on [Gnome Extensions](https://extensions.gnome.org/), and install them with `sudo apt install gnome-shell-extension-<extension-name>`.

### Useful links
* [Debian on the Desktop](https://www.debian.org/devel/debian-desktop/index.en.html)
* [DebianDesktopHowTo](https://wiki.debian.org/DebianDesktopHowTo)
* [How to install and use Debian backports](https://linuxconfig.org/how-to-install-and-use-debian-backports)
