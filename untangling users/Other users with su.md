# Untangling users 

## Other users with su
We are supposed to switch to another user using su and then run a program to get the flag. 

### Solve
**Flag:** `pwn.college{ssSMuo3vcqEcXet4XXxf1djjqHZ.QX2UDN1wSN2gjNzEzW}`

I entered su with the argument of zardus i.e, the user we want to switch to and then entered the user's password. I then ran the program /challenge/run to get the flag. 

```bash
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run 
Congratulations, you have become Zardus! Here is your flag:
pwn.college{ssSMuo3vcqEcXet4XXxf1djjqHZ.QX2UDN1wSN2gjNzEzW}
```

### New Learnings
I learnt how su with an argument lets us change to specific users instead of just the root. 

### References 
None. 
