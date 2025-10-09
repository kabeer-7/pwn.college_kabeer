# Perceiving permissions

## Fun with group names
We are supposed to use id to see the group name and then use chgrp to change the group permissions of the file to get the flag. 

### Solve
**Flag:** `pwn.college{8m__RcqjwVWKFsXHm5s_6cVn_GR.QXycjM1wSN2gjNzEzW}`

This challenge is also similar to the previous ones but the only catch is we have to find our group name which is simple using id. On using id, i could see that my user's group name is grp31658. I then saw which file has the flag using ls -l and then changed the group permissions using chgrp to the group name that we found. I then read the file to get the flag. 

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp31658) groups=1000(grp31658)
hacker@permissions~fun-with-groups-names:~$ ls -l
total 32
-rw-r--r-- 1 hacker grp31658   4 Sep 25 05:15 COLLEGE
-rw-r--r-- 1 hacker grp31658   8 Sep 25 11:03 PWN
-rw-r--r-- 1 hacker grp31658 829 Sep 25 10:36 instructions
-rw-r--r-- 1 root   grp31658  60 Sep 23 05:34 k
-rw-r--r-- 1 hacker grp31658  95 Sep 25 10:36 myflag
lrwxrwxrwx 1 hacker grp31658   5 Sep 27 13:18 not-the-flag -> /flag
drwxr-xr-x 1 hacker grp31658   0 Sep 23 05:29 ok
-rw-r--r-- 1 root   grp31658  77 Sep 29 05:16 okay
-rw-r--r-- 1 hacker grp31658 437 Sep 25 05:31 the-flag
drwxr-xr-x 1 hacker grp31658   0 Sep 23 17:06 tmp
hacker@permissions~fun-with-groups-names:~$ chgrp grp31658 not-the-flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{8m__RcqjwVWKFsXHm5s_6cVn_GR.QXycjM1wSN2gjNzEzW}
```

### New Learnings
Nothing new, just applied our knowledge of id and chgrp to get the flag. 

### References 
None. 
