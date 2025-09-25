# Practising Piping

## Redirecting output
We must use output redirection to write the word PWN to the filename COLLEGE.

### Solve
**Flag:** `pwn.college{ELPvkV1xYi0VUkWQx1Ja5oModLY.QX0YTN0wSN2gjNzEzW}`

I enter 'echo PWN > COLLEGE' as I have to give the output of echo to the file of name COLLEGE. This write PWN in COLLEGE, completing the challenge and hence giving us the flag.  

```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{ELPvkV1xYi0VUkWQx1Ja5oModLY.QX0YTN0wSN2gjNzEzW}
```

### New Learnings
I learnt about the three standards channels of communication in linux: Standard Input, Standard Ouput and Standard Error. In this challenge, we learn how to use output redirection and how we can redirect the output of a command to another file. We are basically redirecting the output to the file instead of displaying the output on the terminal. 

### References 
None. 
