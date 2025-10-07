# Untangling users 

## Becoming root with su
We are supposed to become root with su and enter the given root password while doing so. 

### Solve
**Flag:** `pwn.college{ojWPus7SyFgs1eNgjck89z8IwYF.QX1UDN1wSN2gjNzEzW}`

I entered su and the root password: 'hack-the-planet' to become the root. On using ls, I saw the contents of the directory, which indicated that the flag is in the file 'not-the-flag' as it was highlighted. I simply then got the flag using the cat command. 

```bash
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# ls
COLLEGE  PWN  instructions  k  myflag  not-the-flag  ok  okay  the-flag  tmp
root@users~becoming-root-with-su:/home/hacker# cat not-the-flag 
pwn.college{ojWPus7SyFgs1eNgjck89z8IwYF.QX1UDN1wSN2gjNzEzW}
```

### New Learnings
Learnt how to become the administrative user on a device or root using su and how we can enter passwords for such but modern systems have other methods for protection. 

### References 
None. 
