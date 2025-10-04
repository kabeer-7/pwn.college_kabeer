# Data manipulation

## Sorting Data
We are given a file with 100 flags amongst which is the real one. The real flag is at the end when sorted alphabetically, we must find it. 

### Solve
**Flag:** `pwn.college{QNPukpCsO9XwNDcc5GraGWoiCFd.0FM0MDOxwSN2gjNzEzW}`

I sorted the text from the file reverse alphabetically and hence the flag was the first one. 

```bash
hacker@data~sorting-data:~$ sort -r /challenge/flags.txt 
pwn.college{QNPukpCsO9XwNDcc5GraGWoiCFd.0FM0MDOxwSN2gjNzEzW}
```

### New Learnings
I learnt about the sort program which is used to organise data. It sorts the lines alphabetically on default but different arguments like -r, -n, etc to change the desired output.  

### References 
None. 
