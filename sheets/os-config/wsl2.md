# WSL 2 - Windows Subsystem for Linux

WSL 2, or Windows Subsystem for Linux 2, is a feature of Windows 10 & 11 that allows users to run a Linux kernel directly on Windows, enabling seamless integration between Windows and Linux environments.

## Installation
Enable Windows features
* Sub-system Linux
* Windows Hypervisor Platform

Microsoft Store -> install Debian

## Configuration

To delimiter ressources use :
```bash
#➜  ~ cat /mnt/c/Users/Username/.wslconfig
[wsl2]
memory=4GB
processors=4
```

To handle chmod :
```bash
#➜  ~ cat /etc/wsl.conf
[automount]
options = "metadata"
```

To update or restart WSL
```bash
# PS C:\Users\John Doe> 
wsl --update

# or
wsl --shutdown
```

## Troubleshooting

[Disable Hibernate](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/disable-and-re-enable-hibernation), to remove CPU bug 100%

```bash
# In Cmd (as Administrator)
powercfg.exe /hibernate off
```

## Useful links
* [Windows Subsystem for Linux Documentation](https://learn.microsoft.com/en-us/windows/wsl)
* [Install Linux on Windows with WSL](https://learn.microsoft.com/en-us/windows/wsl/install)
