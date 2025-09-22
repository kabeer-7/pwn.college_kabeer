# Pondering Paths

## Position thy self
The challenge requires us to execute the /challenge/run from a specific path. 

### Solve
**Flag:** `pwn.college{cslyXbNRJaL1XJWwnJ3Oh43xHx4.QX2QTN0wSN2gjNzEzW}`

I input /challenge/run which is incorrect as I do not know the path of the /challenge/run program. The command line tells us that it's incorrect and tells us where the program is located. We need to use 'cd' to change the directory. I enter cd /usr/share/doc. This shifts the current path the shell is at. We will then be able to run the given /challenge/run program and obtain the required flag. 

```bash
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/share/doc
hacker@paths~position-thy-self:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{cslyXbNRJaL1XJWwnJ3Oh43xHx4.QX2QTN0wSN2gjNzEzW}
```

### New Learnings
I learnt how to run a given program using a specific path given. I learnt how to use cd to change the directory to the specific path and run the program. 

### References 
None.
