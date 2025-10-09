# Perceiving permissions

## Changing file ownership
We are supposed to change the file ownership to hacker and read the flag. 

### Solve
**Flag:** `pwn.college{0s5kHwZYEYmdU8HkGoIXa75ZjAF.QXxEjN0wSN2gjNzEzW}`

I just entered the chown command with the hacker user and file /flag and then read the file to get the flag. We didn't need to become root as the hacker user had all the permissions. 

```bash
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{0s5kHwZYEYmdU8HkGoIXa75ZjAF.QXxEjN0wSN2gjNzEzW}
```

### New Learnings
Learnt about how to change the ownership of a file using chown command. Chown stands for changing ownership and literally helps us do so. 

### References 
None.
