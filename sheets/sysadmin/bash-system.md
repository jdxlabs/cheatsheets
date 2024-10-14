# Bash commands focused on system health

## Interactive process viewer
```bash
htop
```

## Show connected hard drives
```bash
df -hT

# or
lsblk
```

## Monitor USB Transfert Rate

### Read
```bash
sudo hdparm -Tt /dev/sdc1
```

### Write
```bash
# todo
```

## Test CPU Usage
```bash
stress -c <nb_cpu> -t 180
```

## Detect failed processes on the system
```bash
systemctl list-units
systemctl list-units --failed
```
