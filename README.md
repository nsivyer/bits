# Nathans one liners and functions

## nmap, fast test of top 5000 ports

    nmap -n -sS -sU -PN --max-retries 1 --min-rate 300 --top-ports 5000 my_host
## beer symbol

    BEER="\xF0\x9F\x8D\xBA"

## encypted vim alias

    alias vime='vim -X -n -N --cmd "set cm=blowfish" --cmd "set nobackup" --cmd "set nowritebackup" --cmd "set key=`. ~/.my_password_file;echo $whatever`"'    

## ssh auto complete

    complete -W "$(ls path_to_hosts_dir |uniq )" ssh

## Debian Colour PS1

    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '

## Kill DNS Cache on OSX

    sudo killall -HUP mDNSResponder

## Transpose one dimetional CSV

    #!/usr/bin/env python
    import sys, csv, itertools
    rows = itertools.izip(*csv.reader(sys.stdin, delimiter=","))
    sys.stdout.writelines(",".join(row) + "\n" for row in rows)

## iptables copy packet to destination

    iptables -t mangle -A POSTROUTING -d 10.0.0.1 -j TEE --gateway 10.0.0.2




