# Direnv

## Install

```bash
mise install direnv@latest

# help
direnv help
```

## Load

```bash
# create a .envrc file
#!/bin/bash
echo "Hello there.."

cd myfolder/
direnv allow
```

## Reload

```bash
direnv reload
```
