# Practising Piping

## Grepping stored results
We are supposed to redirect the output of /challenge/run to /tmp/data.txt and then use grep to find the flag from this file. 

### Solve
**Flag:** `pwn.college{koP7lcZcJ6bw8XiAnR2wG0K8FPa.QX4EDO0wSN2gjNzEzW}`

I did what the challenge asked me to and redirected the output of /challenge/run to /tmp/data.txt which added a few thousand lines of code to data.txt. I then used grep to first search for the keyword flag but was not able to get the flag. Then, on recollection that each flag starts with pwn, I grepped pwn and obtained the flag from the file. 
```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
hacker@piping~grepping-stored-results:~$ grep pwn /tmp/data.txt
pwn.college{koP7lcZcJ6bw8XiAnR2wG0K8FPa.QX4EDO0wSN2gjNzEzW}
pwned
pwning
pwns
pwn

```

### New Learnings
Did not learn anything new, we just learnt more applications of these commands by combining redirection and grepping. 

### References 
None. 
