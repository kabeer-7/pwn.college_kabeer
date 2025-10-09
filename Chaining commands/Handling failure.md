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
Brief note on what you learned from the challenge

### References 
Add any references or videos you used while solving the challenge.
