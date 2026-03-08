# Linux - Void commands

Here are some recipes that might be useful for a Void configuration on your desktop.


## Package manager

```bash
# update repositories :
sudo xbps-install -u xbps
sudo xbps-install -Syu
sudo xbps-install -S

# install a package :
sudo xbps-install -S <pkg>

# remove a package :
sudo xbps-remove -R <pkg>

# search a package (distant) :
xbps-query -Rs <pkg>

# search a package (local) :
xbps-query -l | grep -i <pkg>
```

## Fresh install steps

### Basic programs
```bash
# network
sudo xbps-install -S curl
sudo xbps-install -S falkon
sudo xbps-install -S wireshark-qt

# system
sudo xbps-install -S vim htop ncdu
sudo xbps-install -S fastfetch

# office
sudo xbps-install -S evince
sudo xbps-install -S libreoffice
sudo xbps-install -S gimp
sudo xbps-install -S galculator
sudo xbps-install -S xfce4-screenshooter
sudo xbps-install -S xarchiver unzip 7zip
sudo xbps-install -S void-repo-nonfree && sudo xbps-install -S unrar

# dev
sudo xbps-install -S sublime-text4
sudo xbps-install -S git tree tig
sudo xbps-install -S podman podman-compose

# games
sudo xbps-install -S minigalaxy
sudo xbps-install -S scummvm
sudo xbps-install -S openttd
```

### Partitions

Cfdisk (as Primary)
- Partition EFI : 512M
- Partition Linux Swap : 4G
- Partition Racine Linux(Ext4) : <main> + Bootable flag (si mode DOS != GPT)

Mount points : 
- EFI : vfat/fat32 - /boot/efi
- Swap : swap - none
- Main : ext4 - /

### Lightdm

#### Setup FR @ login :

```bash
sudo vim /etc/lightdm/lightdm.conf
#---
[Seat:*]
display-setup-script=setxkbmap fr
greeter-setup-script=setxkbmap fr
#---
```

#### Auto login :

```bash
sudo vim /etc/lightdm/lightdm.conf
#---
[Seat:*]
autologin-user=<my-name>
autologin-user-timeout=0
#---

# to check that the id exists :
id <my-name>
```

### UI Look

```bash
sudo xbps-install -S arc-theme papirus-icon-theme
```

To make the magic happen, you need to go to two different places in your Settings:
- Go to Appearance
- Style tab: Choose Arc-Dark (for a stylish dark look).
- Icons tab: Choose Papirus-Dark.

Improve the look:
- Right-click on your panel -> Panel Preferences.
- Increase the size (line) to approximately 36.
- Add the "Window Buttons" plugin and configure it to display only icons.


### Printer (for a Canon Pixma TS 5050)

```bash
sudo xbps-install -S cups cnijfilter2 hplip

sudo xbps-install -S \
    cups-filters \
    ghostscript \
    foomatic-db \
    foomatic-db-engine \
    foomatic-db-gutenprint-ppds \
    gutenprint

# start cups
sudo ln -s /etc/sv/cupsd /var/service/
sudo sv up cupsd

# Add admin rights tu current user (and restart cups)
sudo usermod -aG lpadmin $(whoami)
sudo usermod -aG lp $(whoami)
groups $(whoami)  # to check
sudo sv restart cupsd

# configure it in the ui
http://localhost:631

# config / debug
sudo vim /etc/cups/printers.conf
sudo tail -f /var/log/cups/error_log
```


### Install Apps with Flatpak

```bash
# install flatpak and add flathub repository
sudo xbps-install -Sy flatpak
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

# install app
sudo flatpak install flathub <my-app> -y

# launch app
flatpak run <my-app>

# add shortcut in XFCE menu
mkdir -p ~/.local/share/applications
ln -s /var/lib/flatpak/app/<my-app>/current/active/export/share/applications/<my-app>.desktop \
      ~/.local/share/applications/<my-app>.desktop

# manage flatpak apps
# cf. https://docs.flatpak.org/fr/latest/using-flatpak.html
flatpak list
flatpak list --app
flatpak update
flatpak search <my-app>
flatpak uninstall <my-app>
```
