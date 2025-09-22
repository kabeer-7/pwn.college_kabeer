# Pondering Paths

## Program and Absolute Paths
The challenge is similar to the previous one but the program that we are supposed to run is inside the 'challenge' directory. 

### Solve
**Flag:** `pwn.college{kB_7BY06oJE1LoM3svXvzDMdpic.QX1QTN0wSN2gjNzEzW}`

In this challenge, the program that we are supposed to run is named 'run'. It is been given that challenge program is in the '/challenge' directory. So, I provided the absolute path to the program i.e, '/challenge/run'. On providing the path, we get the required flag. 

```bash
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{kB_7BY06oJE1LoM3svXvzDMdpic.QX1QTN0wSN2gjNzEzW}
```

### New Learnings
We only further learn how to run a program in a directory after /. 

### References 
None. 
