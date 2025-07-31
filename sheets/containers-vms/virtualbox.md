# VirtualBox

## Install on Windows

```
PS (Admin)
choco install virtualbox
```

And get Extension Pack (for ui improvements)  
here : https://www.virtualbox.org/wiki/Downloads


## Debian Install specs

- 20 Gb, one mount point
- 4 Gb
- 2 cpus
- install NAT (for SSH : https://dev.to/developertharun/easy-way-to-ssh-into-virtualbox-machine-any-os-just-x-steps-5d9i)
- Install a shared folder
- set host key : MAJ + RIGHT ALT


## Install guest additions

```
cd /mnt/folder
sudo sh VBoxScript.run
```

## SSH into the instance
```
ssh -p 3022 myuser@127.0.0.1
```
