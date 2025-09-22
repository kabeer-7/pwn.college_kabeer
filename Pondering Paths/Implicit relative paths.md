# Pondering Paths

## Implicit relative paths
We need to run /challenge/run using a relative path while having a current working directory of /. 

### Solve
**Flag:** `pwn.college{IiXNFmReEtQ54n8cR2Mm93qk5bQ.QX5QTN0wSN2gjNzEzW}`

We change the directory using cd to '/' and then run 'challenge/run'. / is the selected directory and hence we only need to run chalenge/run instead of running /challenge/run. 

```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{IiXNFmReEtQ54n8cR2Mm93qk5bQ.QX5QTN0wSN2gjNzEzW}

```

### New Learnings
I learnt how to use implicit relative paths and how we ran the program /challenge/run with respect to the path /. 

### References 
none.
