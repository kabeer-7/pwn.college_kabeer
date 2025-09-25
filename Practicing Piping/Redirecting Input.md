# Practising Piping

## Redirecting input
We are supposed make the file PWN contain the value COLLEGE and then redirect the PWN file as input to the program /challenge/run. 

### Solve
**Flag:** `pwn.college{c-ptvL3Hwg-g6_GcbtpoIVU64N2.QXwcTN0wSN2gjNzEzW}`

Using echo I redirected the value COLLEGE into PWN and then redirected the PWN file as input to the program /challenge/run which then reads the file PWN to see the value COLLEGE and hence gives us the flag. 

```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{c-ptvL3Hwg-g6_GcbtpoIVU64N2.QXwcTN0wSN2gjNzEzW}
```

### New Learnings
I learnt about how to redirect input to programs rather than output from programs. 

### References 
None. 
