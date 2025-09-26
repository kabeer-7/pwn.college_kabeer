# Shell variables

## Exporting variables
We must export PWN with its value as COLLEGE and set COLLEGE as PWN but not export it. We must then run /challenge/run. 

### Solve
**Flag:** `pwn.college{gVvDebRioHEqBRmsh07AoDBy3z9.QXyYTN0wSN2gjNzEzW}`

I exported PWN with the value COLLEGE, this sets the value of PWN as COLLEGE into the environment variables of child processes. I then set the value of COLLEGE as PWN which means it is only set locally. I then open a child shell line to run /challenge/run. This satisfies what is asked of us and gives the flag. 
```bash
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ sh
sh-5.2$ /challenge/run 
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{gVvDebRioHEqBRmsh07AoDBy3z9.QXyYTN0wSN2gjNzEzW}

```

### New Learnings
Learnt about child shell or minimal shell. Got to know how our variables are only saved locally and we have to use the export command to pass the value of variables into the environment variable sof child processes. 

### References 
None. 
