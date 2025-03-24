# Mise

[Mise](https://mise.jdx.dev/) is a utility written in Rust, with the same principles thant [ASDF](https://asdf-vm.com/).

Install :
```bash
curl https://mise.run | sh
echo "eval \"\$(/home/user/.local/bin/mise activate zsh)\"" >> "/home/user/.zshrc"
```

Commands : 
```bash
mise version
mise --help

# install
mise use node@latest
mise use python@latest
mise use terraform@latest
mise use opentofu@latest

# install cloud clients
mise use awscli@latest
mise use gcloud@latest

# show installed software
mise ls

# show available software
mise ls-remote terraform
mise ls-remote terraform@1.11

# updates
mise up --interactive
```


# UV - Python package manager (in Rust)

```bash
mise use uv@latest

uv pip --help
# or
uv help pip

# install requests globally
uv pip install requests --system
```
