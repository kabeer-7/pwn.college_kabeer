# Pondering Paths

## Explicit relative paths, from /
With / as our current working directory, we have to run the /challenge/run program using . in our relative path. 

### Solve
**Flag:** `pwn.college{8KW9HmrnpsFreCoVcrAUHWQKhPv.QXwUTN0wSN2gjNzEzW}`

Since we are to use / as our current working directory, I enter cd / to change the current working directory to /. I, then enter ./challenge/run where . indicates the current working directory ie, /. Entering this commandd, I get the required flag. 

```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{8KW9HmrnpsFreCoVcrAUHWQKhPv.QXwUTN0wSN2gjNzEzW}
```

### New Learnings
I learnt the use of '..' and '.' which are used to shorten the command. Instead of providing the complete path from the root directory or from the relative path, we can use '..' and '.' where '..' refers to the parent directory one level up and '.' refers to the current working directory. 

### References 
Used AI to understand the application of '..' and '.'. 
