# Processes and jobs

## Backgrounding processes
We are supposed suspend a process and then run it's copy while another one runs in the background.

### Solve
**Flag:** `pwn.college{stUVrtSQciUXC5sNnaRzuxmRDmV.QX3QDO0wSN2gjNzEzW}`

I simply started the process /challenge/run, suspended it using ctrl+z, then resumed it in the background by entering bg. I then ran a copy of the process which gave me the flag.  

```bash
hacker@processes~backgrounding-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         162 S+   bash /challenge/run
root         164 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$ 


Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run 
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         162 S    bash /challenge/run
root         172 S    sleep 6h
root         173 S+   bash /challenge/run
root         175 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{stUVrtSQciUXC5sNnaRzuxmRDmV.QX3QDO0wSN2gjNzEzW}
```

### New Learnings
Learnt about how to resume a suspended process in the background using bg. 

### References 
None. 
