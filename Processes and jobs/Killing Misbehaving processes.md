# Processes and jobs

## Killing misbehaving processes
Add challenge description here

### Solve
**Flag:** `pwn.college{MMinZRpAexaBnQjxhTjGhZuC8Q8.0FNzMDOxwSN2gjNzEzW}`

I first listed all the processes related to decoy and found the PID value for /challenge/decoy (142). On killing the process, I run /challenge/run which sent the flag to /tmp/flag_fifo. I used cat to read contents of the fifo which contained lots of decoy flags. I terminated the process and ran /challenge/run again which sent the flag to the fifo. On reading the fifo again, I could see the required flag. 

```bash
hacker@processes~killing-misbehaving-processes:~$ ps aux | grep decoy
root         139  0.0  0.0   5204  3520 ?        S    14:52   0:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
hacker       142  0.0  0.0  13516  9280 ?        Ss   14:52   0:00 /usr/bin/python /challenge/decoy
hacker       189  0.0  0.0 230696  2560 pts/0    S+   14:58   0:00 grep --color=auto decoy
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run 
Sending the flag to /tmp/flag_fifo!
^C
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
hacker@processes~killing-misbehaving-processes:~$ /challenge/run 
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo 
pwn.college{MMinZRpAexaBnQjxhTjGhZuC8Q8.0FNzMDOxwSN2gjNzEzW}
^C

```

### New Learnings
Nothing new, just applied what was learnt from the previous challenges. 

### References 
None. 
