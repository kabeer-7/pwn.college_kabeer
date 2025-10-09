# Perceiving permissions

## Changing permissions
We must change the permissions of /flag to read it. 

### Solve
**Flag:** `pwn.college{0ZkTtW1hB5BVRG2YpMtrWzHnhVS.QXzcjM1wSN2gjNzEzW}`

I entered chmod ugo+rwx giving my user,group and others the permission to read,write and execute the file. I then read the file to get the flag. 

```bash
hacker@permissions~changing-permissions:~$ chmod ugo+rwx not-the-flag 
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{0ZkTtW1hB5BVRG2YpMtrWzHnhVS.QXzcjM1wSN2gjNzEzW}
```

### New Learnings
Understood how to change the permission of a file using chmod. 

### References 
None. 
