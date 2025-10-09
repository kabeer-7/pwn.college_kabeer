# Perceiving permissions

## The SUID bit
We are supposed to add suid to the program and then read the flag. 

### Solve
**Flag:** `pwn.college{MDMkzUvyjbXdaGesPNjP9of7od6.QXzEjN0wSN2gjNzEzW}`

I first added the suid to /challenge/getroot and then ran it, this spanned a root shell for me to cat /flag to get the flag. 

```bash
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot 
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{MDMkzUvyjbXdaGesPNjP9of7od6.QXzEjN0wSN2gjNzEzW}
```

### New Learnings
Learnt about SUID and how we can add SUID to a file as owners of the file so that other users can read the file. 

### References 
None. 
