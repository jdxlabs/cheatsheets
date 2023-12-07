# Some configuration tips for Windows 10

## Software
You can find a list of tools to work under Windows 10 on the [[software-equivalents|Software equivalents]] page.

If you need to test some functionalities of Windows on your machine, Microsoft delivers [[https://developer.microsoft.com/fr-fr/windows/downloads/virtual-machines|official evaluation VMs valid for 2 months]].

## PowerShell command line under Windows
If you want to automate things under Windows there is the [[powershell|PowerShell]] language you can use, that offers strong proximity with the system.

## Linux development under Windows
If you want to have a Linux development environment under Windows, you can use [[wsl2|WSL2]], or set a [[windows10-vagrant|Vagrant configuration]], that works with VirtualBox and offers full VM configuration of any Linux distribution.

You may also prefer to work with Docker for Windows, with Linux support.
## Install package managers
```bash

# Chocolatey install
PS(Admin) > Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

# Scoop install (more "unix-flavored")
PS(User) > iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

## Install basic tools
```bash
PS(Admin) >
# for a new pc
choco install -y libreoffice notepadplusplus vlc sumatrapdf XnViewMP 7zip wiztree

# for developers
choco install -y  git cmder vscode vagrant virtualbox docker


PS(Admin) > scoop install wget curl sudo ruby python

# If you installed Git, you can access Bash from anywhere in Powershell
PS > & 'C:\Program Files\Git\bin\sh.exe'
```
