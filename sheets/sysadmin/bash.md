# Bash

## Get disk space usage
```bash
df -h
```

## Get a clean arborescence of a projet
```bash
tree -a -I '.git' -L 3
```

## Get the size of elements in the current folder
```bash
du -chs *
```

## Find largest directories in current path
```bashdu -ck | sort -nr | head -n 10```

## Get working path
```bashpwd```

## Get system infos
```bash
uname -a
lsb_release -a
```

## Grep search
```bashgrep -ril mot_a_chercher .```

## Restart a service
```bash
# examples :
sudo /etc/init.d/nom_du_service restart
sudo service nom_du_service restart
apache2ctl restart
```

## Delete files older than 30 days, in the current folder
```bashfind . -maxdepth 1 -ctime +29 -exec rm {} \;```

## Delete ".svn" folders, from current path
```bashfind . -name ".svn" -type d -exec rm -rf {} \;```

## Get "png" files, from current path
```bashfind . -iname '*.png'```

## Count nb of files, in the current path
```bashfind . -type f | wc -l```

## Search a term in a serie of files
```bashgrep -nri (my_term) ~/logs_*```

## Compress dir
```bashtar -zcvf tar-archive-name.tar.gz source-folder-name```

## Uncompress dir
```bashtar -zxvf tar-archive-name.tar.gz source-folder-name```

## Anacron (daily)
```bash
sudo apt-get install anacron
sudo vim /etc/cron.daily/newfile
( | tee -a /var/log/anacron_newfile.log)
```

## Auto upgrade sur Anacron (daily)
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


# Related resources :
  * [[https://devhints.io/bash|DevHints - Bash]]

