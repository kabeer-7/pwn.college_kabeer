# Chaining commands

## Building on success
We are supposed to chain two processes using &&.

### Solve
**Flag:** `pwn.college{saN_duKq8sP0Rk30O1XjB54erDT.0lM0MDOxwSN2gjNzEzW}`

```bash
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second 
Nice chaining! Flag: pwn.college{saN_duKq8sP0Rk30O1XjB54erDT.0lM0MDOxwSN2gjNzEzW}
```

### New Learnings
Learnt about chaining with &&. This only executes the second process if the first one exits with a code 0 ie, it was successful. 

### References 
None. 
