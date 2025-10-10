# Pondering Path

## The PATH variable
We are supposed to remove the path to the rm command so on running /challenge/run, the flag doesn't get deleted and we get it. 

### Solve
**Flag:** `pwn.college{g-AR63dZp_--jPb48UzzPXrZDZQ.QX2cDM1wSN2gjNzEzW}`

I just removed the PATH variable so rm could not be found and hence this gave me the flag when I ran /challenge/run. 

```bash
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run 
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{g-AR63dZp_--jPb48UzzPXrZDZQ.QX2cDM1wSN2gjNzEzW}
```

### New Learnings
Learnt about the PATH varibale which assists the shell in finding where the file, for the command we are running, is. 

### References 
None. 
