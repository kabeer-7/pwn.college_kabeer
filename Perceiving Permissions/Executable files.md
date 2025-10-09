# Perceiving permissions

## Executable files
We must make the program executable and then run it to get the flag.

### Solve
**Flag:** `pwn.college{MeS0JKp6Nrpy1VjfsKSLesMWjgU.QXyEjN0wSN2gjNzEzW}`

I used chmod to make the program executable for everybody and then ran the program to get the flag. 

```bash
hacker@permissions~executable-files:~$ chmod ugo+x /challenge/run 
hacker@permissions~executable-files:~$ /challenge/run 
Successful execution! Here is your flag:
pwn.college{MeS0JKp6Nrpy1VjfsKSLesMWjgU.QXyEjN0wSN2gjNzEzW}
```

### New Learnings
Nothing new, just applied what was learnt previously to make a file executable on top of readable. 

### References 
None. 
