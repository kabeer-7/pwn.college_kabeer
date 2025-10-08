# Untangling users 

## Using sudo 
We are supposed to use sudo access to read the flag. 

### Solve
**Flag:** `pwn.college{Mbj47qq6aZlkLRg9gk2VXMSZaa9.QX4UDN1wSN2gjNzEzW}`

I used ls to see the contents of the directory and then used sudo cat to read not-the-flag which was highlighted. This gave me the flag. 

```bash
hacker@users~using-sudo:~$ ls
COLLEGE  PWN  instructions  k  myflag  not-the-flag  ok  okay  the-flag  tmp
hacker@users~using-sudo:~$ sudo cat not-the-flag 
pwn.college{Mbj47qq6aZlkLRg9gk2VXMSZaa9.QX4UDN1wSN2gjNzEzW}
```

### New Learnings
Learnt about sudo and how it runs commands as root rather than switching the user to root which is not viable all the time. 

### References 
None. 
