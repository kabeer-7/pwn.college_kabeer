# Chaining commands

## Executable shell scripts
We are supposed to invoke /challenge/solve using shell script, and then run it without explicitly, invoking bash.

### Solve
**Flag:** `pwn.college{Uvo2GbBb97uDgfJ_nxl09lSS2bg.QX0cjM1wSN2gjNzEzW}`

I used echo to create a self script which invokes the program and change its permissions so that it could be executed without root or bash. I then simply entered the path of the Shell script and hence executed the program which gave me the flag.

```bash
hacker@chaining~executable-shell-scripts:~$ echo /challenge/solve > x.sh
hacker@chaining~executable-shell-scripts:~$ chmod u+xwr x.sh 
hacker@chaining~executable-shell-scripts:~$ ./x.sh 
Congratulations on your shell script execution! Your flag:
pwn.college{Uvo2GbBb97uDgfJ_nxl09lSS2bg.QX0cjM1wSN2gjNzEzW}
```

### New Learnings
Learnt how to execute shell scripts without the use of bash by changing the permissions of the shell script. 

### References 
None. 
