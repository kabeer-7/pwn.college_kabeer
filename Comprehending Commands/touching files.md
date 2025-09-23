# Comprehending Commands

## Touching Files
The challenge asks us to create two blank files pwn and college in the tmp directory using the touch command, after which we run /challenge/run to obtain the flag. 

### Solve
**Flag:** `pwn.college{Yhu5YMPbw-VZnOaLPAB4Bv8sQHf.QXwMDO0wSN2gjNzEzW}`

First, I changed the current working directory to tmp using cd so that i can create the files under tmp. Using touch, I created the files pwn and college. To make sure that the files were created, I use ls to see the contents of the directory. After creating the two files, I go back to the home directory and run /challenge/run to obtain the flag. 

```bash
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ ls
bin  college  hsperfdata_root  pwn  tmp.TpSOPGOVKK
hacker@commands~touching-files:/tmp$ cd
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{Yhu5YMPbw-VZnOaLPAB4Bv8sQHf.QXwMDO0wSN2gjNzEzW}
```

### New Learnings
Learnt about the touch command which is primarily used to create blank files in the directory of our choice. 

### References 
None. 
