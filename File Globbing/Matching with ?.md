# File Globbing

## Matching with ?
Change the directory to /challenge using ? instead of the letters c and l. Then we have to run /challenge/run to get the flag. 

### Solve
**Flag:** `pwn.college{Ardgq0Xw7vfrGwJIDe2JZ15kf_k.QXyIDO0wSN2gjNzEzW}`

I simply replaced c and l with ? in the argument to cd to change the directory and then ran /challenge/run (in the same way) to obtain the required flag. 

```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /?ha??enge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{Ardgq0Xw7vfrGwJIDe2JZ15kf_k.QXyIDO0wSN2gjNzEzW}

```

### New Learnings
I learnt about ? which functions the same way as * but only replaces single characters and not all patterns like *. 

### References 
None. 
