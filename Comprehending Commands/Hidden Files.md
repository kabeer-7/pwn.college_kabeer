# Comprehending Commands

## Hidden Files
We need to find the hidden flag, hidden as a dot-prepended file in /. 

### Solve
**Flag:** `pwn.college{UZl8NsemI9FQ0CWd26rzNhnnS5j.QXwUDO0wSN2gjNzEzW}`

I changed the current working directory to / using cd and then I used the ls command with the -a flag to see all the files including the ones which start with a '.'. I can then see that there is a file called '.flag-17856286836463' which can be acesssed using the cat command hence returning the required flag. 

```bash
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-17856286836463  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-17856286836463 
pwn.college{UZl8NsemI9FQ0CWd26rzNhnnS5j.QXwUDO0wSN2gjNzEzW}
```

### New Learnings
The ls command doesn't list all the files by default, it doesn't list the files starting with '.' by default. We need to invoke ls with -a flag to view these hidden files. In this challenge we were able to find the hidden flag using this same command and flag, teaching us how to access all contents of a directory. 

### References 
None. 
