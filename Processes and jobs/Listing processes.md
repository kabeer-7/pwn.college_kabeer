# Processes and jobs

## Listing processes 
A program has been run. We have to use ps command to obtain list of processes and get the filename. We will be obtaining the file when the program 

### Solve
**Flag:** `pwn.college{I7M8yQDcGEE8p5hfUi426LbCIej.QX4MDO0wSN2gjNzEzW}`

I entered ps -ef to see all processes, from which I found a process starting with the word challenge. After running it, I obtained the flag. 

```bash
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 13:05 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-i
root           7       1  0 13:05 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 13:05 ?        00:00:00 /challenge/14711-run-24327
root         135     132  0 13:05 ?        00:00:00 sleep 6h
hacker       146       1  0 13:05 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --po
hacker       150     146  0 13:05 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       160       0  0 13:05 pts/1    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       166     160  0 13:05 pts/1    00:00:00 /run/dojo/bin/bash --login
hacker       175     166  0 13:06 pts/1    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/14711-run-24327
Yahaha, you found me! Here is your flag:
pwn.college{I7M8yQDcGEE8p5hfUi426LbCIej.QX4MDO0wSN2gjNzEzW}
Now I will sleep for a while (so that you could find me with 'ps').
```

### New Learnings
I learnt about the ps command and it's arguments. ps is used to display current running processes in the command line. In the -ef argument, -e is used to display all user processes and -f is used to display them in full format. Similarly, we have another argument to ps which is aux. In aux, a shows processes for all users, u displays the info in a user-oriented manner and x includes processes not attached to the terminal

### References 
None.
