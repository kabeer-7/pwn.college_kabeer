# Comprehending Commands

## Removing Files
This challenge asks us to remove the 'delete_me' file that was created in our home directory. Running /challenge/check will verify if it's removed and then give us the flag. 

### Solve
**Flag:** `pwn.college{oTUI88gtlHHZo7PVsG-pUYIzSGQ.QX2kDM1wSN2gjNzEzW}`

Having learnt that rm command is used to remove files, I entered 'rm delete_me' and hence the file delete_me was removed. I, then, ran /challenge/check which checked if the file was removed and returned back with the flag. 

```bash
hacker@commands~removing-files:~$ rm delete_me 
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{oTUI88gtlHHZo7PVsG-pUYIzSGQ.QX2kDM1wSN2gjNzEzW}
```

### New Learnings
I learnt the rm command which is used to remove files in the linux command line.  

### References 
Add any references or videos you used while solving the challenge.

