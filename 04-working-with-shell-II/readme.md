# 04 Working with Shell - II

## Behind Schedule

## File compression and archival

### Viewing file sizes
```console
    du -sk test.img
    1000000000000

    du -sh testimg
    98M test.img

    ls -lh test.img

    -rw-rw-r-- 1 99M Mar 13 15:30 test.img

```

### ARchiving Files

```console
    tar -cf test.tar file1 file2 file3
    ls -ltr test.tar

    tar -tf test.tar

    tar-xf test.tar

    tar-zcf
```

### Compressing

#### bzip2
```console
    bzip2 test.img

    du-sh test.img.bz2
```

#### gzip
```console
    gzip test1.img

    du -sh test1.img.gz
```

#### xz
```console
    xz test2.img

    du -sh test2.img.xz
```

### Uncompressing

#### bunzip2
```console
    bunzip2 test.img.bz2

    du -sh test.img
```

#### gunzip
```console
    gunzip test1.img.gz

    du -sh test1.img
```

#### unxz
```console

    unxz test2.img.xz

    du -sh test2.img

```

## Searching for files and pattern

locate
```console
    locate city.txt
```

updatedb
```console
    updatedb
```

find
```console
    find /home/getsemani -n getse.txt
```

### GREP

```console
    grep second sample.txt

    Followed by the second line

    cat sample.txt

    grep -i capital sample.xt

    grep -r "third line" /home/chael

    grep -v  "printed" sample.txt
```

## IO Redirection

## Vi Editor