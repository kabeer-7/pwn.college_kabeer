# Shell variables

## Storing command output
we must read the output of /challenge/run directly into the PWN variable.

### Solve
**Flag:** `pwn.college{wpTclV1W7-eEUSFABD7A-A8cx2m.QX1cDN1wSN2gjNzEzW}`

I used command substitution to set variable PWN's value to the output of /challenge/run which was the flag. I then printed out the variable's value and got the flag. 

```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{wpTclV1W7-eEUSFABD7A-A8cx2m.QX1cDN1wSN2gjNzEzW}
```

### New Learnings
Learnt about command subtitution which helps us store the output of some command directly into a variable using $(). 

### References 
None. 
