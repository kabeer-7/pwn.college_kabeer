# Comprehending Commands

## Making directories
we are required to create a /tmp/pwn directory and make a file college in it. We then run /challenge/run to check our solution and give us the flag. 

### Solve
**Flag:** `pwn.college{cgc16U80dlo3xMJyMhTDO0o1OhE.QXxMDO0wSN2gjNzEzW}`

I created the tmp directory in the home directory and changed the current working directory to it using cd. I, then, created the pwn directory in tmp and changed the directory to it using cd. Then, I created the file college using the touch command and then run the /challenge/run to check the program and give us the flag.                   

```bash
hacker@commands~making-directories:~$ mkdir tmp
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls
college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{cgc16U80dlo3xMJyMhTDO0o1OhE.QXxMDO0wSN2gjNzEzW}
```

### New Learnings
I learnt the mkdir command to create directories. 

### References 
None. 
