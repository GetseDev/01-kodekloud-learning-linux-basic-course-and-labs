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

# SSH and SCP

# IPTABLES Introduction

# IpTables - Securing the Enviroment

# Cronjobs