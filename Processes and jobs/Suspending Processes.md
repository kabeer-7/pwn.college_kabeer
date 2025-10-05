# Processes and jobs

## Suspending Processes 
We were asked to suspend the process and then run a copy of the process, this will give the flag. 

### Solve
**Flag:** `pwn.college{81ZGz0Rcobaj8-nVDM8jOULv3vy.QX1QDO0wSN2gjNzEzW}`

I ran /challenge/run and then suspended it using ctrl+z. Running /challenge/run gave the flag. 

```bash
hacker@processes~suspending-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         162     129  0 15:11 pts/0    00:00:00 bash /challenge/run
root         164     162  0 15:11 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         162     129  0 15:11 pts/0    00:00:00 bash /challenge/run
root         169     129  0 15:11 pts/0    00:00:00 bash /challenge/run
root         171     169  0 15:11 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{81ZGz0Rcobaj8-nVDM8jOULv3vy.QX1QDO0wSN2gjNzEzW}
```

### New Learnings
Learnt about how to use ctrl+z to suspend processes to the background.

### References 
None. 
