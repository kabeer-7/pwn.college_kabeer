# Terminal Multiplexing

## Switching windows (tmux)
We have two windows in the session where window 0 has the flag and window 1 is the welcome message. We must swtich windows to get the flag. 

### Solve
**Flag:** `pwn.college{kqlgriAcgbB_pbq7JJv1ZDa6Z7u.0FM5IDOxwSN2gjNzEzW}`

Did the same as the previous switching windows challenge. I connected to the session made for us using tmux attach and switched to the welcome window which told me that the flag is in window 0. I switched to window zero using ctrl+b and 0. This gave me the flag.

```bash
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux attach
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Welcome to the tmux window switching challenge!
> You are currently in window 1.
> The flag is hidden in window 0.
> Use Ctrl-B 0 to switch to window 0!
> MSG
Welcome to the tmux window switching challenge!
You are currently in window 1.
The flag is hidden in window 0.
Use Ctrl-B 0 to switch to window 0!
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{kqlgriAcgbB_pbq7JJv1ZDa6Z7u.0FM5IDOxwSN2gjNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{kqlgriAcgbB_pbq7JJv1ZDa6Z7u.0FM5IDOxwSN2gjNzEzW}
```

### New Learnings
Just the same as screen but with ctrl+b.

### References 
None. 
