# Terminal Multiplexing

## Switching windows
We have a session with 2 windows where window 1 has a welcome message and window 0 is unknown. We are supposed to then find the flag. 

### Solve
**Flag:** `flag: pwn.college{8IgjUQO2YFyp0gBVBT17jyVZYBk.0FO4IDOxwSN2gjNzEzW}`

I connected to the session made for us using screen -r and switched to the welcome window which told me that the flag is in window 0. I switched to window zero using ctrl+a and 0. This gave me the flag. 
```bash
hacker@terminal-multiplexing~switching-windows:~$ screen -r
[screen is terminating]
 cat <<MSG
Welcome to the window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-A 0 to switch to window 0!
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{8IgjUQO2YFyp0gBVBT17jyVZYBk.0FO4IDOxwSN2gjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{8IgjUQO2YFyp0gBVBT17jyVZYBk.0FO4IDOxwSN2gjNzEzW}
```

### New Learnings
Learnt about switching windows using keyboard shortcuts all starting with ctrl+a. 

### References 
None.
