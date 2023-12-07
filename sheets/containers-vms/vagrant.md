# Hashicorp Vagrant

Installation

```bash
# First, install Virtualbox, then :

# On mac
brew install hashicorp/tap/hashicorp-vagrant


# On windows WSL2 (with Debian/Ubuntu distro)
wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install vagrant

# Then, there is a plugin for Vagrant :
vagrant plugin install virtualbox_WSL2

~/.zshrc
export VAGRANT_WSL_ENABLE_WINDOWS_ACCESS="1"

/etc/wsl.conf
[automount]
options = "metadata"

```


Useful commands

```bash
vagrant up
vagrant status
vagrant ssh my-machine
vagrant provision

vagrant halt
vagrant destroy -f
```


