# Bash commands focused on network

## Install network tools

### Debian
```bash
apt install -y iputils-ping # for ping
apt install -y dnsutils # for dig, etc.
apt install -y net-tools # for netstat, etc.
apt install -y nmap
```

### CentOS
```bash
yum install -y bind-utils # for nslookup, etc.
yum install -y nmap # for ncat, etc.
```

## Basic commands
```bash
# Show current IP address
ip address
# or
ifconfig -a

# Informations about an url
ping example.com
traceroute example.com
```

## Lookup DNS for an url
```bash
dig <any_url>
```

## Show the IPs connected to a machine
```bash
netstat -ntpul
```

## Show listening ports & processes on a machine
```bash
lsof -i -P -n
lsof -i -P -n | grep LISTEN
```

## Netcat : check if 2 machines are able to communicate on a specified port
```bash
nc -l -p 1337 # the receiver
nc localhost 1337 # the sender
# then type something, then enter, it should be transfered to the receiver
```

## Ping an IP on a particular port

### Telnet method
```bash
telnet 15.0.0.93 4648
```

### Nmap method (/!\ may bypass restrictions)
```bash
nmap -Pn -p 4648 15.0.0.93
```

## Find the IPs connected on the same LAN

### Nmap method
```bash
nmap -sP <current_ip>/24
```
### ARP method
```bash
sudo arp-scan --interface=<current_interface> --localnet
```

## TcpDump

```bash
tcpdump -i any host 10.0.5.37
tcpdump -i any port 443
tcpdump -i any port 443 and host 10.0.0.1 or host 10.0.0.2 or host 10.0.0.3
tcpdump -ni any port 443 and host 10.0.0.1 or host 10.0.0.2 or host 10.0.0.3
```

## IpTables

```bash
iptables -L -t nat

# Flush all
iptables -F -t nat
```

## Calculate CIDRs

```bash
apt install ipcalc

ipcalc -b 244.178.44.111 24

# or
apt install sipcalc
sipcalc 244.178.44.111/24
```

## Usefull links
* [Linux networking tools](https://gist.github.com/miglen/70765e663c48ae0544da08c07006791f)
* [Every Linux networking tool I know](https://twitter.com/icheikhrouhou/status/1133049722384601089)
