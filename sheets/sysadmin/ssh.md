# SSH commands

## Create private/public key on the current machine
```bash
ssh-keygen -t rsa

# another cypher :
ssh-keygen -t ed25519
```

## Copy the public key on a distant server
```bash
ssh-copy-id -i ~/.ssh/id_rsa.pub user@server
```

## Remove all keys belonging to hostname from a known_hosts file
```bash
ssh-keygen -R hostname
```

## SSH : Copy file
```bash
scp [name@server:][FROM] [name@server:][TO]
```

## SSH : Copy directory
```bash
scp -rp [name@server:][FROM] [name@server:][TO]
```


