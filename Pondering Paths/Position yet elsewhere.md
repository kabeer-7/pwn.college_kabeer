# Pondering Paths

## Position yet elsewhere
The challenge requires us to execute the /challenge/run from a specific path.

### Solve
**Flag:** `pwn.college{U6dR1w2R3xwomeyHFKL6SCfyKTT.QX4QTN0wSN2gjNzEzW}`

This challenge includes the same thought process as the previous two challenges. Upon running the /challenge/run program, the command line gives the correct directory of the program i.e, the /var directory. Upon changing the directory to /var using cd /var, I enter the /challenge/run program which executes it and returns the required flag. 
```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /var directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /var
hacker@paths~position-yet-elsewhere:/var$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{U6dR1w2R3xwomeyHFKL6SCfyKTT.QX4QTN0wSN2gjNzEzW}
```

### New Learnings
Nothing new learnt on top of the previous challenges. Just changed directory to the given specific path to execute the given program. 

### References 
None.
