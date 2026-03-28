# VirtualBox

## Install on Windows

```
PS (Admin)
choco install virtualbox virtualbox-extensionpack
```

You can also find installation files from the official website here : 
https://www.virtualbox.org/wiki/Downloads.

Extension Pack will add more features to your VirtualBox, 
like USB 3.0 support, RDP, disk encryption, etc.


## Debian Install specs

- 16 Gb, one mount point
- 4 Gb ram
- 2 cpus
- install NAT #2 (for SSH : port forwarding 3022:22)
- Install a shared folder
- set host key : MAJ + RIGHT ALT


## Install guest additions



```bash
# Install the dependencies
sudo apt update
sudo apt install build-essential dkms linux-headers-$(uname -r)

# Insert Guest Additions CD image from the VirtualBox menu (Devices > Insert Guest Additions CD image)

# Then, go to the folder where you downloaded the VBoxScript.run file, and run the following command :
cd /media/path/to/VBoxScript.run
sudo sh VBoxScript.run
```

## SSH into the instance

Activate port forwarding in the VirtualBox settings (NAT #2 : 3022:22), then you can SSH into the instance with the following command :

```bash
ssh -p 3022 myuser@127.0.0.1
```

# Useful links
- [VirtualBox Documentation](https://www.virtualbox.org/manual/)
- [VirtualBox Extension Pack](https://www.virtualbox.org/wiki/Downloads)
- [Installing VirtualBox Guest Additions](https://lecrabeinfo.net/tutoriels/virtualbox-installer-les-additions-invite-guest-additions/#sur-une-machine-virtuelle-linux)
- [SSH into VirtualBox](https://dev.to/developertharun/easy-way-to-ssh-into-virtualbox-machine-any-os-just-x-steps-5d9i)
- [VirtualBox Shared Folders](https://www.virtualbox.org/manual/ch04.html#sharedfolders)
- [VirtualBox Networking](https://www.virtualbox.org/manual/ch06.html)
