# Gitlab cmds


## Install the cli

```bash
mise install glab@latest
```

## Connect to your instance

```bash
glab auth login --hostname gitlab.com --device

```

## Check your username

```bash
glab api user --hostname gitlab.com | grep -i username
```
