# Processes and jobs

## Foregrounding processes
We are supposed foreground a background process. 

### Solve
**Flag:** `pwn.college{4w8L0Ic0pHIKbI5Ed6s0qAu1Ms_.QX4QDO0wSN2gjNzEzW}`

I ran the process, suspended it and then resumed it in the background using bg. On entering fg, I foregrounded the background process and got the flag. 

```bash
hacker@processes~foregrounding-processes:~$ /challenge/run 
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{4w8L0Ic0pHIKbI5Ed6s0qAu1Ms_.QX4QDO0wSN2gjNzEzW}
```

### New Learnings
Learnt how fg can be used to foreground a background process on top of resuming suspended processes. 

### References 
None. 
