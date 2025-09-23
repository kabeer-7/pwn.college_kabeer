# Comprehending Commands

## Hidden Files
We need to find the hidden flag, hidden as a dot-prepended file in /. 

### Solve
**Flag:** `pwn.college{UZl8NsemI9FQ0CWd26rzNhnnS5j.QXwUDO0wSN2gjNzEzW}`

I use the ls command with the -a flag to see all the files including the ones which start with a '.'. 

```bash
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-17856286836463  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-17856286836463 
pwn.college{UZl8NsemI9FQ0CWd26rzNhnnS5j.QXwUDO0wSN2gjNzEzW}
```

### New Learnings
Brief note on what you learned from the challenge

### References 
Add any references or videos you used while solving the challenge.
