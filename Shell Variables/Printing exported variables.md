# Shell variables

## Printing exported variables
We are supposed to use env command to get the flag. 

### Solve
**Flag:** `pwn.college{gID2A-nLR2WQJHluemkcCYvPfv7.QX4UTN0wSN2gjNzEzW}`

I enter env which is a command that prints out every exported variable set. The flag was amongst the output.

```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=ea7da834de69099b2b38fe32d0a3bd8a05814bee0776d932bdc5e5a94de78fba
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{gID2A-nLR2WQJHluemkcCYvPfv7.QX4UTN0wSN2gjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

### New Learnings
We get to know about the env command that prints out every exported variable set in our shell. 

### References 
None. 
