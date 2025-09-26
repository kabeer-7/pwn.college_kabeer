# Shell variables

## Reading input
we must use read to set the PWN variable to the value COLLEGE.

### Solve
**Flag:** `pwn.college{cWoprQXHecVcotE7l5t_vtxVUZh.QX4cTN0wSN2gjNzEzW}`

I simply entered 'read PWN' which according to the syntax means that the shell is asking for input for the variable PWN.  
```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{cWoprQXHecVcotE7l5t_vtxVUZh.QX4cTN0wSN2gjNzEzW}
```

### New Learnings
Learnt about the read command which is used to take input from the user and with the -p argument lets you specify a prompt. 

### References 
None. 
