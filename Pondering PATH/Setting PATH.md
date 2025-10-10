# Pondering Path

## Setting PATH 
We are supposed to set the PATH to the given directory to be able to run /challenge/run which will invoke the win command to get the flag. 

### Solve
**Flag:** `pwn.college{YrK-jzNM9HfVyTSxNE4TR2ul--p.QX1cjM1wSN2gjNzEzW}`

I set the PATH to /challenge/more_commands/ in which the win command is included. Hence, on running /challenge/run, the win command could be run which gave us the flag. 

```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run 
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{YrK-jzNM9HfVyTSxNE4TR2ul--p.QX1cjM1wSN2gjNzEzW}
```

### New Learnings
Learnt how to set the PATH.

### References 
None. 
