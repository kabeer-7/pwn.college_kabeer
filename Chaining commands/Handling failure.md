# Chaining commands

## Handling failure
We need to chain /challenge/first-failure and /challenge/second using the || operator. 

### Solve
**Flag:** `pwn.college{cAPcwdpeUiO-U0PbSwmTWzGW5DC.01M0MDOxwSN2gjNzEzW}`

```bash
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second 
Nice chaining! Flag: pwn.college{cAPcwdpeUiO-U0PbSwmTWzGW5DC.01M0MDOxwSN2gjNzEzW}
```

### New Learnings
Learnt about || operator which is the opposite of the && operator and runs only if the first command/process fails or exits with a non-zero code. 

### References 
None
