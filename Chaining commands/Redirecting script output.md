# Chaining commands

## Redirecting script output
We are supposed to add the two programs to the shell script and then redirect the output of the shell script as input to /challenge/solve to get the flag. 

### Solve
**Flag:** `pwn.college{411AnRXZyP6fQvUAgT7y4uOCjgC.QX4ETO0wSN2gjNzEzW}`

I did what was asked, added the two programs to the shell script as in the previous challenge. I then piped the output of the shell script to /challenge/solve to get the flag. 

```bash
hacker@chaining~redirecting-script-output:~$  echo '/challenge/pwn ; /challenge/college' > x.sh
hacker@chaining~redirecting-script-output:~$ bash x.sh | /challenge/solve 
Correct! Here is your flag:
pwn.college{411AnRXZyP6fQvUAgT7y4uOCjgC.QX4ETO0wSN2gjNzEzW}
```

### New Learnings
Understood that piping output from a shell script can be useful when multiple commands are needed to be inputted into a command or program. 

### References 
None. 
