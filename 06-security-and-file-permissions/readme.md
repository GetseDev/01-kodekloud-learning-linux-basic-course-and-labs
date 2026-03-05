# Linux Accounts

Linux Security -> Access Control, PAM, Network Security, SSH Hardning, SELinux, Many More

Users -> Username getse, UID 1000, GID 1000, Home Directory /homme/getsemani, Default Shell /bin/sh

```console

    id michael

    grep -i michael /etc/passwd

```

Superuser Account -> Root, UID = 0
System Accounts -> Ssh, Mail. UID < 100 or Between 500 - 1000
Service Accounts -> nginx, mercury

cat /etc/passwd

Groups

cat /etc/passwd

## Commands

Information user
```console
    id

    who

    last
```

## Swhiching Users

```console
    su -i 

    su -c "whoami" 
```

## SUDO

visudo -> /etc/sudoers

```console
    cat /etc/sudoers
```

# Access Control Files

```console
    grep -i ^bob /etc/passwd
```

# User Management

## Managing Users

```console
    useradd getse

    grep -i getse /etc/passw

    grep -i getse /etc/shadow

    paasw getse
```

```console
    useradd -u 1009 -g 10009 -d /home/getse -s /bin/bash -c "Mercury Project Member" getse
```

-c Custom Comments
-d Custom Home Directory
-e Expiry Date
-g specific GID
-G create user with multiple secondary groups
-s specify login shells
-u specific UID

```console
    userdel getse

    groupadd -g 1011 developer

    group del developer
```

# File Permissions and Ownership

```console
    ls -l bash-script.sh
```

file type | identifier
directory | d
regular file | - 
character device | c
link | |
socket file | s
PIPE | p
Block Device | b

- rwxrwxr - x
owner = u
group = g
others = o

bit | purpose | octal value
r | read | 4
w | write | 2
x | execute | 1
- | no permission | 0 

## Modifying File Permissions

chmod <permissions> file

chmod u+rwx test-file -> provide full access to owner
chmod ugo+r-x test-file -> provide read access to owner group and others, remove execute access
chmod o-rwx test-file -> remove all access for others
chmod u+rwx,g+r-x,o-rwx test file -> full access for owner, add read, remove execute for group and no access for others

chown owner:group file

chown bob:developer file -> changes owner to bob and group to developer
chown bob android apk -> changes just the owner of the file to bob. group unchanged
chgrp android test-file -> change the group for the test-file to the group called android

# SSH and SCP



# IPTABLES Introduction

# IpTables - Securing the Enviroment

iptables -A INPUT -p tcp -s 172.16.238.187 --dport 22 -j ACCEPT

sudo iptables -A INPUT -p tcp -s 172.16.238.187 --dport 22 -j ACCEPT
sudo iptables -A INPUT -p http -s 172.16.238.187 --dport 80 -j ACCEPT


sudo iptables -A INPUT -p tcp -s 172.16.238.10 --dport 22 -j ACCEPT
sudo iptables -A INPUT -p tcp -s 172.16.238.11 --dport 22 -j ACCEPT
sudo iptables -A INPUT -p tcp -s 172.16.238.06 --dport 22 -j ACCEPT

# Cronjobs

uptime >> /tmp/system_report.txt
