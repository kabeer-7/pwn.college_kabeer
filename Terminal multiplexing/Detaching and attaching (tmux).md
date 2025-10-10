# Terminal Multiplexing

## Detaching and attaching (tmux)
We are supposed to launch tmux, detach from it, run /challenge/run and then reattach to the session to see the flag. 

### Solve
**Flag:** `pwn.college{EuHBMeYSoup_Lany5XqYKKam3ER.0VO4IDOxwSN2gjNzEzW}`

Same as the previvous detaching and attaching challenge but used tmux with ctrl+b. First launched tmux and detached using ctrl+b and b. I then ran /challenge/run which sent the flag to the session. I then reattached to the session using tmux attach and got the flag. 

```bash
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux
[detached (from session 0)]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run 
Found detached tmux session: 0
Sending flag to your tmux session...

Flag sent! Now reattach to your tmux session with:
  tmux attach

You'll find the flag waiting for you there!
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux attach
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{EuHBMeYSoup_Lany5XqYKKam3ER.0VO4IDOxwSN2gjNzEzW}
Congratulations, here is your flag: pwn.college{EuHBMeYSoup_Lany5XqYKKam3ER.0VO4IDOxwSN2gjNzEzW}
```

### New Learnings
Just learnt about tmux and how it uses ctrl+b instead of ctrl+a in screen. 

### References 
None. 
