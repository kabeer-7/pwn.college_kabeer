# Terminal mulyiplexing 

## Detaching and attaching 
We are supposed to launch screen, detach from it and then run /challenge/run which will send the flag to the detached session. We are then supposed to reconnect to the session. 

### Solve
**Flag:** pwn.college{Ukb-gNY4JDubsvX2-8h5-tallSm.0lN4IDOxwSN2gjNzEzW}`

I basically first entered screen to launch a session and then detached using ctrl-a and then entering d for detach. I then ran the program in the original session which sent the flag to the detached session. On reconnecting to the session using screen -r, we get the flag.   

```
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen
[detached from 162.pts-0.terminal-multiplexing~detaching-and-attaching]
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run 
Found detached screen session: 162.pts-0.terminal-multiplexing~detaching-and-attaching
Sending flag to your screen session...

Flag sent! Now reattach to your screen session with:

  screen -r

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{Ukb-gNY4JDubsvX2-8h5-tallSm.0lN4IDOxwSN2gjNzEzW}
Yes! Flag is: pwn.college{Ukb-gNY4JDubsvX2-8h5-tallSm.0lN4IDOxwSN2gjNzEzW}
```

### New Learnings
Learnt how to detach from a session and how to recconnect to it using ctrl-a with d and screen -r respectively. 

### References 
None. 