# Comprehending Commands

## Listing files
We are supposed to list the files under /challenge to find what the required program file is called and hence run it to obtain the required flag. 

### Solve
**Flag:** `pwn.college{wqB99CnDpneUPVpLmgE6qQno5UR.QX4IDO0wSN2gjNzEzW}`

I used ls to list all the files under /challenge to see what the run file has been renamed to. Here, it was renamed to 26199-renamed-run-5622. On running /challenge/26199-renamed-run-5622 , i get the desired flag. 
```bash
hacker@commands~listing-files:~$ ls /challenge
26199-renamed-run-5622  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/26199-renamed-run-5622 
Yahaha, you found me! Here is your flag:
pwn.college{wqB99CnDpneUPVpLmgE6qQno5UR.QX4IDO0wSN2gjNzEzW}
```

### New Learnings
I learnt how ls is used to list the content of a directory and how it may help us navigate the contents of a directory. 

### References 
None. 
