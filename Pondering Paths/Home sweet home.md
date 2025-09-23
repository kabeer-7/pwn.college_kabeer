# Pondering Paths

## Home sweet Home
The challenge /challenge/run will write a copy of the flag to any file you specify as an argument on the commandline, with these constraints:

Your argument must be an absolute path.
The path must be inside your home directory.
Before expansion, your argument must be three characters or less.

We are then required to specify our path as an argument to /challenge/run. 

### Solve
**Flag:** `pwn.college{EBkUecNhgUTEeWDOL_EgwN3WChh.QXzMDO0wSN2gjNzEzW}`

I enter ~/k as an absolute path to a file in our home directory which also satisfies the constraint of the argument being 3 characters or less. The explansion of this is /home/hacker/k. After executing this command, the /challenge/run program recieves the path and writes the flag to the file 'k'. 

```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/k
Writing the file to /home/hacker/k!
... and reading it back to you:
pwn.college{EBkUecNhgUTEeWDOL_EgwN3WChh.QXzMDO0wSN2gjNzEzW}
```

### New Learnings
I learnt how shell expansion works and how ~ is a symbol referring to the user's home directory, in this case ~ is /home/hacker. I also got to know how to solve the challenge satsifying the constraints given. 

### References 
none. 
