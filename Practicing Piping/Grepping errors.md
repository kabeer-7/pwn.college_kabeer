# Practising Piping

## Grepping errors
We are supposed to change the fd from 1 to 2 so that we can pipe the errors from /challenge/run and grep for the flag. 

### Solve
**Flag:** `pwn.college{QLEKqnF20RWysz6GGbR_qu3uqaO.QX1ATO0wSN2gjNzEzW}`

I simply wrote the command using the resources given. 2>&1 redirects the file descriptor from 1 to 2 so we can read the errors from the program while using grep. 

```bash
hacker@piping~grepping-errors:~$ /challenge/run 2>&1  | grep pwn

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwned
pwn
pwn.college{QLEKqnF20RWysz6GGbR_qu3uqaO.QX1ATO0wSN2gjNzEzW}
pwning
pwns

```

### New Learnings
Piping only provides standard output and file descriptors can be redirected to each other using >& in piping. 

### References 
None. 
