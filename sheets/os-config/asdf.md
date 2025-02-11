# Mise

[ASDF](https://asdf-vm.com/) is a utility to manage all your runtime versions with one tool.

Install :
```bash
# Installing dependencies
sudo apt install curl git unzip

# Download asdf
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.14.1

# Install asdf
cat >> ~/.bashrc <<EOF
# ASDF
. "\$HOME/.asdf/asdf.sh"
. "\$HOME/.asdf/completions/asdf.bash"
EOF
source ~/.bashrc
```

Commands : 
```bash
asdf version
asdf --help

# add plugins
asdf plugin add terraform 1.6.2
asdf plugin add terraform-docs
asdf plugin add terragrunt
asdf plugin add tflint
asdf plugin add direnv

cat .tool-versions       
terraform 1.6.2
terraform-docs 0.17.0
terragrunt 0.55.1
tflint 0.50.1
direnv 2.35.0

# install versions of plugins (following the closest ".tool-versions" file)
asdf install

# show installed plugins
asdf plugin list
asdf plugin list --urls

# remove plugin
asdf plugin remove direnv

# show current version of plugins
asdf current
asdf current terraform

# list available versions of plugins
asdf list-all terraform

# change plugin version locally/globally
asdf global terraform 1.6.2
asdf local terraform 1.7.5

# update plugins
asdf plugin update --all
```

## Useful links
* [ASDF - Commands](https://asdf-vm.com/manage/commands.html)
* [asdf Basics & Cheat Sheet](https://dev.to/tanminator/asdf-basics-cheat-sheet-hn8)
