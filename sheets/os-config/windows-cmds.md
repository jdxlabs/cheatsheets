# Windows commands tips

## PowerShell : Windows Automation Tool
If you want to automate things under Windows there is the PowerShell language you can use,  
that offers strong proximity with the system.

## Bash commands under Windows
If you want to have a Linux development environment under Windows, you have this possibilities : 
- Use Git bash (the best way, if you are very restricted on rights)
- Use Docker for Windows, with Linux support
- Use WSL2 - Windows Subsystem for Linux 2 (the best way, if you have enough rights)

## Package managers : Chocolatey and Scoop

### Chocolatey install
```bash
PS(Admin) > Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

### Scoop install (more "unix-flavored")
```bash
PS(User) > iex (new-object net.webclient).downloadstring('https://get.scoop.sh')
```

## Package managers : Install packages

### Chocolatey commands
```bash
PS(Admin) >
choco install -y libreoffice notepadplusplus vlc sumatrapdf XnViewMP 7zip

# more
choco install -y skype discord steam cpu-z hwinfo scanner wiztree gimp homebank keepassxc pcloud protonvpn

# dev
choco install -y vscode filezilla notion

# music / multimedia
choco install -y reaper guitar-pro obs-studio shotcut

# uninstall packages
choco uninstall shotcut

# show outdated packages
choco outdated

# upgrades
choco upgrade chocolatey
choco upgrade cpu-z

# upgrade all outdated packages
choco upgrade all
```

### Dev tools
```bash
PS(Admin) > 
choco install -y git cmder vscode vagrant virtualbox docker
scoop install wget curl sudo ruby python
```

### Bash access from PowerShell (once Git is installed)
If you installed Git, you can access Bash from anywhere in Powershell
```bash
PS > & 'C:\Program Files\Git\bin\sh.exe'
```

## Useful links
* [Windows technical documentation for developers and IT pros](https://learn.microsoft.com/en-us/windows/)
* [Get a Windows 11 development environment (valid for 2 months)](https://developer.microsoft.com/en-us/windows/downloads/virtual-machines)
..
