# Debian Desktop tips

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

## Useful links
* [Debian on the Desktop](https://www.debian.org/devel/debian-desktop/index.en.html)
* [DebianDesktopHowTo](https://wiki.debian.org/DebianDesktopHowTo)
* [How to install and use Debian backports](https://linuxconfig.org/how-to-install-and-use-debian-backports)
