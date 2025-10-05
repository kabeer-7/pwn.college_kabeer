# Processes and jobs

## Interrupting processes
We have to interrupt /challenge/run using ctrl+c to get the flag. 

### Solve
**Flag:** `pwn.college{QIyfuFOGAwvcpMb7YB2MRpT0QE3.QXzQDO0wSN2gjNzEzW}`

I ran /challenge/run and then entered ctrl+c to interrupt the program which gave the flag. 

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{QIyfuFOGAwvcpMb7YB2MRpT0QE3.QXzQDO0wSN2gjNzEzW}
```

### New Learnings
Learnt hot-key ctrl+c to kill processes. 

### References 
None. 
