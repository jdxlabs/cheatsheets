# Bash

## Get disk space usage

```bash
df -h
```

## Get a clean arborescence of a projet

```bash
trae -a

tree -a -I '.git'  # ignoring .git folder
tree -a -I '.git' -L 3  # ignoring .git folder, and limiting to 3 levels
```

## Get the size of elements in the current folder

```bash
du -chs *
```

## Find largest directories in current path

```bash
du -ck | sort -nr | head -n 10
```

## Get working path

```bash
pwd
```

## Get system infos

```bash
uname -a
lsb_release -a
```

## Grep search

```bash
grep -ril mot_a_chercher .
```

## Restart a service

```bash
/etc/init.d/service_name restart
service service_name restart
```

## Delete files older than 30 days, in the current folder

```bash
find . -maxdepth 1 -ctime +29 -exec rm {} \;
```

## Delete ".svn" folders, from current path

```bash
find . -name ".svn" -type d -exec rm -rf {} \;
```

## Get "png" files, from current path

```bash
find . -iname '*.png'
```

## Count nb of files, in the current path

```bash
find . -type f | wc -l
```

## Search a term in a serie of files

```bash
grep -nri (my_term) ~/logs_*
```

## Compress dir

```bash
tar -zcvf tar-archive-name.tar.gz source-folder-name
```

## Uncompress dir

```bash
tar -zxvf tar-archive-name.tar.gz source-folder-name
```

## Anacron (daily)

```bash
sudo apt-get install anacron
sudo vim /etc/cron.daily/newfile
( | tee -a /var/log/anacron_newfile.log)
```

## Anacron auto upgrade (daily)

```bash
~ cat /etc/cron.daily/auto-upgrade 
#!/bin/sh

date | tee -a /var/log/anacron_auto-upgrade.log
apt-get -y update && apt-get -y upgrade | tee -a /var/log/anacron_auto-upgrade.log
```

## Make a diff between 2 folders

```bash
diff -bur <folder1> <folder2>
```

## Update root password

```bash
sudo passwd <username>
```

## Add a user to sudoers

```bash
vim /etc/sudoers.d/{{ user }}-sudoer
{{ user }} ALL=(ALL:ALL) NOPASSWD: ALL

# or if you want to keep password protection (more secure) :
{{ user }} ALL=(ALL:ALL) ALL
```

## Add a script to execute at startup

```bash
vim /etc/init.d/rc.local
{{ anything }}
```

## Update default programs

```bash
sudo update-alternatives --all
```

## Print a part of a file

```bash
sed -n 20,40p myfile
```

## Zip / unzip a folder

```bash
zip -r myfile.zip mydir
unzip myfile.zip

# alternative : zip directly to the root folder
cd mydir/ && zip ../myfile.zip -r .
```

## Execute a command in background

```bash
<any-command>  > /dev/null 2>&1 &
```

## Security : Generate a GPG key

```bash
gpg --gen-key
```

## Get a clean arborescence of a projet

```bash
tree -a -I '.git' -L 3
```

## Usefull links
* [Bash Reference Manual](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html)
* [DevHints - Bash](https://devhints.io/bash)
