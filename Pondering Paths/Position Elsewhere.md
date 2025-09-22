# Pondering Paths

## Position Elsewhere
The challenge requires us to execute the /challenge/run from a specific path.

### Solve
**Flag:** `pwn.college{U-a41vZAyfzSYs2Dfko7AFvDFND.QX3QTN0wSN2gjNzEzW}`

This challenge is pretty much the same as the previous challenge i.e, position thy self except the directory. I input /challenge/run which is incorrect as I do not know the path of the /challenge/run program. The command line tells us that it's incorrect and tells us where the program is located. We need to use 'cd' to change the directory. I enter cd /etc/apt/sources.list.d. This shifts the current path the shell is at. We will then be able to run the given /challenge/run program and obtain the required flag.

```bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /etc/apt/sources.list.d directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /etc/apt/sources.list.d
hacker@paths~position-elsewhere:/etc/apt/sources.list.d$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{U-a41vZAyfzSYs2Dfko7AFvDFND.QX3QTN0wSN2gjNzEzW}
```

### New Learnings
Learnt nothing new on top of the previous challenge. 

### References 
None. 
