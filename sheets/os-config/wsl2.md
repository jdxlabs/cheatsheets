# WSL 2 (Windows Subsystem for Linux)

[[https://learn.microsoft.com/en-us/windows/wsl/install|WSL2]] is a Linux implementation for Windows.

## Activation

Microsoft Store -> install Debian

Enable or disable Windows features
  * Sub-system Linux
  * Windows Hypervisor Platform

## Configuration
```bash
➜  ~ cat /mnt/c/Users/Username/.wslconfig
[wsl2]
memory=4GB
processors=4

# to handle chmod :
➜  ~ cat /etc/wsl.conf
[automount]
options = "metadata"
```

## Update / Restart
```bash
PS C:\Users\John Doe> 
wsl --update
wsl --shutdown
```

## Troubleshooting

Disable Hibernate, to remove CPU bug 100% :

https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/disable-and-re-enable-hibernation

