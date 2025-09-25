# Practising Piping

## Grepping live output
We are supposed to grep the program for the flag while it outputs live. 

### Solve
**Flag:** `pwn.college{8TVoeN3hYK5fK6340b8DCvqN1Y-.QX5EDO0wSN2gjNzEzW}`

I used what was taught and using piping grepped the output of the program live for the keyword pwn which got me the flag. 

```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn

pwning
pwned
pwn.college{8TVoeN3hYK5fK6340b8DCvqN1Y-.QX5EDO0wSN2gjNzEzW}
pwns
pwn

```

### New Learnings
Learnt how piping works as it inputs the output of the left side to the right side simultaneously reducing time and need for more files like in the previosu challenge.

### References 
None. 
