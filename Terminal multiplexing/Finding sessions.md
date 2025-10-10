# Terminal Multiplexing 

## Finding sessions 
We are given 3 sessions which we're supposed to connect to and find the flag (which is in one session) by trial and error. 

### Solve
**Flag:** `pwn.college{helloworld}`

I used 'screen -ls' to see the available sessions and then connected to each one using 'screen -r session_name'. On connecting to the right session, I got the flag. 

```bash
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls
There are screens on:
	144.session_e807851d79b453a1	(Detached)
	147.session_c41046e554f94faf	(Detached)
	150.session_96ea0936a011da54	(Detached)
3 Sockets in /home/hacker/.screen.
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_e807851d79b453a1
[screen is terminating]
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_c41046e554f94faf
[screen is terminating]
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_96ea0936a011da54
[screen is terminating]
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{YzTkwlbn3fcq9VZ7cKrBjE28ihI.01N4IDOxwSN2gjNzEzW}
pwn.college{YzTkwlbn3fcq9VZ7cKrBjE28ihI.01N4IDOxwSN2gjNzEzW}
```

### New Learnings
Learnt how to find sessions and list them out using screen -ls. We can then connect to specific sessions using 'screen -r session_name'. 

### References 
None. 
