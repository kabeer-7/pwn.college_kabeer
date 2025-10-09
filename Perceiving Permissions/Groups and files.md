# Perceiving permissions

## Groups and files
We are supposed to change the group ownership to hacker and then read the flag. 

### Solve
**Flag:** `pwn.college{YL3MzDwln9ywnZ7PDjRpO1kZpYJ.QXxcjM1wSN2gjNzEzW}`

Similar to the last challenge, I changed the group ownership to hacker and read the /flag file to get the flag. 

```bash
hacker@permissions~groups-and-files:~$ chgrp hacker not-the-flag
hacker@permissions~groups-and-files:~$ cat /flag 
pwn.college{YL3MzDwln9ywnZ7PDjRpO1kZpYJ.QXxcjM1wSN2gjNzEzW}
```

### New Learnings
I learnt about the id command which lets us see which groups we're a part of and how to change group ownership using chgrp command. 

### References 
None. 
