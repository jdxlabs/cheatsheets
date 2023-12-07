# Some configuration tips for Debian

## Software
You can find a list of tools to work under Debian on the [[software-equivalents|Software equivalents]] page.

## Install process
  * [[https://linuxconfig.org/how-to-install-and-use-debian-backports|How to install and use Debian backports]]
  * [[https://www.debian.org/devel/debian-desktop/index.en.html|Debian on the Desktop]]
  * [[https://wiki.debian.org/DebianDesktopHowTo|DebianDesktopHowTo]]
  * [[http://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/|Unofficial non-free images including firmware packages]]
  * [[https://wiki.debian.org/InstallingDebianOn/Dell/Dell_XPS_13_9380|Installing Debian On Dell XPS 13 9380]]
  * [[linux-stellar-pc-ekimia|Debian install on Stellar PC from Ekimia (2017)]]

## Extract a Debian archive
```bash
ar x dpkg_1.17.23_amd64.deb
tar -zxf data.tar.gz
(or tar -xf data.tar.xz)
```

## Set the locale timezone
```bash
dpkg-reconfigure tzdata
```

## Add an icon for an application (ex: Postman)
```bash
cat > ~/.local/share/applications/Postman.desktop <<EOL
[Desktop Entry]
Type=Application
Name=Postman
Exec=/home/jdx/.local/bin/postman
Icon=/home/jdx/dev/progs/Postman/app/resources/app/assets/icon.png
Categories=Development;
Encoding=UTF-8
Terminal=false
EOL
```

## Dark Gnome theme compatibility with Firefox
Add this file to handle dark themes with Firefox : 
```bash
cat ~/.mozilla/firefox/randomName.default/chrome/userContent.css
input:not(.tactile-searchbox-input):not(.urlbar-input):not(.textbox-input):not(.form-control):not([type='checkbox']) {
    -moz-appearance: none !important;
    background-color: white;
    color: black;
}

#downloads-indicator-counter {
    color: white;
}

textarea {
    -moz-appearance: none !important;
    background-color: white;
    color: black;
}

select {
    -moz-appearance: none !important;
    background-color: white;
    color: black;
}
```

## Update FlashPlayer (while it's useful !)

Download the tar.gz archive from the [[https://get.adobe.com/fr/flashplayer/|official website]], then :
```bash
tar -xzvf flash_player_npapi_linux.x86_64.tar.gz
sudo mv libflashplayer.so /usr/lib/mozilla/plugins

# rm -rf flash_player_npapi_linux.x86_64.tar.gz LGPL license.pdf readme.txt usr
```
