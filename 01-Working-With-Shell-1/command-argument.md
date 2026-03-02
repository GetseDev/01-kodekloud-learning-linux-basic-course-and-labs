
# Command and Argument

`bash
    echo
`

`bash
    echo Hello
`

`bash
    uptime
`

`bash
    echo -n Hello
`


`

    command <options> <arguments>

    echo = command
    option = -n 
    Hello = Argument
    
`

#Command Types

Internal or Built-in commands

```console
    echo, cd, pwd, set, etc..
```

```console
    type echo

    echo is a shell built-in
```

External commands
```console
    mv, date, uptime, cp, etc...
```

```console
    type mv

    mv is hashed (/bin/mv)
```


# Basic Linux Commands

pwd (present working directory)

```console

    pwd
    /home/michael
```

Ls (List Contents)
```console
    ls
```

mkdir (make a new directory)
```console
    mkdir Asia
```

mkdir (multiple directories)
```console
    mkdir Europe Africa America
```

Create directory subdirectory if exists Mumbai
```console
    mkdir -p India/Mumbai
```

Create subdirectory on India
```console
    mkdir India/Mumbai
```

## Absoule and Relative Path 

(/) -> (home) -> (michael) -> (Asia)

```console
    cd = change directory
```

```console
    pwd = print present working directory
```

### Absolute Path
```console
    cd /home/michael/Asia
```

### Relative Path
```console
    cd Asia
```

## Pro Tip - pushd/popd

pushd /etc

push ->
pop <-

```console
    pushd /etc

    cd /var
    cd /tmp
```

```console
    popd

```
```console
    mv Europe/Morocco Africa
```

Copy File with Mumbai in City.txt and move to Cairo
```console
    cp Asia/India/Mumbai/City.txt Africa/Egypt/Cairo

    cat Africa/Egypt/Cairo/City.txt
    city
```

Delete file in London with archive Tottenham.txt 
```console
    rm Europe/UK/London/Tottenham.txt
```

Copy Directory 

```console
    cp -r Europe/UK Europe/UnitedKingdom
```

cat (redirect)
```console
     cat > Africa/Egypt/Cairo/City.txt


```

touch (create a new file)
```console
    touch touch Asia/China/Country.txt
```

## LS (Long List)

ls -l (long list)
```console
    ls -l

    ╰─ ls -l
total 1083012
drwxr-xr-x 26 getse getse      4096 Sep 26 18:01  FaktorCapital
-rw-r--r--  1 getse getse         0 Oct  8 22:15  FaktorCapital.zip:Zone.Identifier
drwxr-xr-x  9 getse getse      4096 Oct  9 00:02  FaktorCapitalV2
-rw-r--r--  1 getse getse        24 Oct 12 16:07  README.md
drwxr-xr-x  3 getse getse      4096 Nov  2 21:13  __MACOSX
-rw-r--r--  1 getse getse       410 Jul 22  2025  acceso-aws.txt
-rw-r--r--  1 getse getse      3090 Oct 23 22:14  alertways-audiences.env
drwxr-xr-x  3 getse getse      4096 Nov  2 21:57  aws
drwxr-xr-x  6 getse getse      4096 Dec 19 22:22  aws-terraform-microservices-lab
-rw-r--r--  1 getse getse      1675 Oct 19 09:26  bastion-canada.pem
-rw-r--r--  1 getse getse  44798584 Oct 22 00:09  build.zip
-rw-r--r--  1 getse getse         0 Oct 22 00:09  build.zip:Zone.Identifier
drwxr-xr-x  4 getse getse      4096 Oct 26 18:30  cf-alertways
-rw-r--r--  1 getse getse     43218 Oct 23 22:34  cf-alertways.zip
-rw-r--r--  1 getse getse         0 Oct 23 22:34  cf-alertways.zip
```

ls -a (list all files including hidding)
```console
    ls -a

    ╰─ ls -a
 .                                   FaktorCapitalV2
 ..                                  README.md
 .aws                                __MACOSX
 .azure                              acceso-aws.txt
 .bash_history                       alertways-audiences.env
 .bash_logout                        aws
 .bashrc                             aws-terraform-microservices-lab
 .cache                              bastion-canada.pem
 .codex                              build.zip
 .config                             build.zip:Zone.Identifier
 .copilot                            cf-alertways
 .docker                             cf-alertways.zip
 .dotnet                             cf-alertways.zip:Zone.Identifier
 .git-credentials                    citi
```
ls -lt (long list files in order created)
```console
╰─ ls -lt
total 1083012
drwxr-xr-x  3 getse getse      4096 Feb 27 23:40  kodekloud
drwxr-xr-x  8 getse getse      4096 Feb  4 22:05  cursos
drwxr-xr-x  2 getse getse      4096 Jan 27 22:58  curso-vpc-network
drwxr-xr-x  3 getse getse      4096 Jan 13 20:01  script
-rw-r--r--  1 getse getse       743 Jan 13 20:00  test.cjs:Zone.Identifier
drwxr-xr-x  6 getse getse      4096 Dec 19 22:22  aws-terraform-microservices-lab
drwxr-xr-x  7 getse getse      4096 Dec 19 21:44  practicas-devops
drwxr-xr-x  5 getse getse      4096 Dec  2 10:50  citi
drwxr-xr-x  3 getse getse      4096 Nov 10 21:41  proyectos-backend
drwxr-xr-x  5 getse getse      4096 Nov 10 21:39  venv
drwxr-xr-x  3 getse getse      4096 Nov  2 21:57  aws
drwxr-xr-x  3 getse getse      4096 Nov  2 21:31  webapp-aws-control
drwxr-xr-x  3 getse getse      4096 Nov  2 21:13  __MACOSX
-rw-r--r--  1 getse getse         0 Nov  2 21:13  webapp-aws-c
```

ls -ltr order files in order reverse

```console
╰─ ls -lt
total 1083012
drwxr-xr-x  3 getse getse      4096 Feb 27 23:40  kodekloud
drwxr-xr-x  8 getse getse      4096 Feb  4 22:05  cursos
drwxr-xr-x  2 getse getse      4096 Jan 27 22:58  curso-vpc-network
drwxr-xr-x  3 getse getse      4096 Jan 13 20:01  script
-rw-r--r--  1 getse getse       743 Jan 13 20:00  test.cjs:Zone.Identifier
drwxr-xr-x  6 getse getse      4096 Dec 19 22:22  aws-terraform-microservices-lab
drwxr-xr-x  7 getse getse      4096 Dec 19 21:44  practicas-devops
drwxr-xr-x  5 getse getse      4096 Dec  2 10:50  citi
drwxr-xr-x  3 getse getse      4096 Nov 10 21:41  proyectos-backend
drwxr-xr-x  5 getse getse      4096 Nov 10 21:39  venv
drwxr-xr-x  3 getse getse      4096 Nov  2 21:57  aws
drwxr-xr-x  3 getse getse      4096 Nov  2 21:31  webapp-aws-co
```

# Using command line to get help

```console
    whatis date
date (1)             - print or set the system date and time
```

```console
    man date

    
NAME
       date - print or set the system date and time

SYNOPSIS
       date [OPTION]... [+FORMAT]
       date [-u|--utc|--universal] [MMDDhhmm[[CC]YY][.ss]]

DESCRIPTION
       Display date and time in the given FORMAT.  With -s, or with [MMDDhhmm[[CC]YY][.ss]], set the
       date and time.

       Mandatory arguments to long options are mandatory for short options too.

       -d, --date=STRING
              display time described by STRING, not 'now'

       --debug
              annotate the parsed date, and warn about questionable usage to stderr

       -f, --file=DATEFILE
              like --date; once for each line of DATEFILE

       -I[FMT], --iso-8601[=FMT]

```

## Using command line to get help

```console
    ╰─ date --help
Usage: date [OPTION]... [+FORMAT]
  or:  date [-u|--utc|--universal] [MMDDhhmm[[CC]YY][.ss]]
Display date and time in the given FORMAT.
With -s, or with [MMDDhhmm[[CC]YY][.ss]], set the date and time.

Mandatory arguments to long options are mandatory for short options too.
  -d, --date=STRING          display time described by STRING, not 'now'
      --debug                annotate the parsed date,
                              and warn about questionable usage to stderr
  -f, --file=DATEFILE        like --date; once for each line of DATEFILE
  -I[FMT], --iso-8601[=FMT]  output date/time in ISO 8601 format.
                               FMT='date' for date only (the defau
```

```console
apropos modpr
modprobe (8)         - Add and remove modules from the Linux Kernel
modprobe.d (5)       - Configuration directory for modprobe

```

# Bash Shell

## Shell Types
Bourne Shell (sh)
C Shell (csh or tcsh)
Korn Shell (ksh)
Z Shell (zsh)
Bourne Again Shell (bash)

## Bash Shell Features

### Bash Auto Completion

```console
    ─ ls FaktorCapital/
    FaktorCapital/
    FaktorCapital.zip:Zone.Identifier
    FaktorCapitalV2/
    README.md
    __MACOSX/
    acceso-aws.txt
    alertways-audiences.env
```

### Alias
```console
alias dt=date

dt
Sat Feb 28 14:56:42 PST 2026

```

### History

```console
history
    1  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    2  clear
    3  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    4  git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
    5  clear
    6  sudo rm
```

### Bash Enviroment Variables

```console
echo $SHELL
/usr/bin/zsh
```

```console
    env
```

```console
    export OFFICE=caleston
```

### Path Variable

```console
echo $PATH
/home/getse/.nvm/versions/node/v20.19.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/wsl/lib:/mnt/c/Program Files (x86)/Microsoft SDKs/Azure/CLI2/wbin:/mnt/c/WINDOWS/system32:/mnt/c/WINDOWS:/mnt/c/WINDOWS/System32/Wbem:/mnt/c/WINDOWS/System32/WindowsPowerShell/v1.0/:/mnt/c/WINDOWS/System32/OpenSSH/:/mnt/c/Program Files/dotnet/:/mnt/c/Program Files/Git/cmd:/mnt/c/Program Files (x86)/Google
```

```console
which terraform
/usr/bin/terraform
```

```console
    export PATH=$PATH:/opt/obs/bin
```

## Bash Promp

```console
     ~ = PResent Working Directory
     $ = User Prompt Symbol

     \W = Present Working Directory = ~
     $ = Prompt Symbol
```
echo 'export PS1='[\d]\u@\h:\w$'' >> ~/.profile

echo 'alias up="uptime"' >> ~/.profile

export PS1='[\d]\u@\h:\w$'
export PS1="[\u@\h \D{%F} %T \w]\$ "