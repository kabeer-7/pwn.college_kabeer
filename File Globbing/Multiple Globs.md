# File Globbing

## Multiple globs
We are supposed to run /challenge/run with an argument using multiple globs to cover all words that contain p. 

### Solve
**Flag:** `pwn.college{UO7OPRMTqNvbQC1fD2eLEtPlbOi.0lM3kjNxwSN2gjNzEzW}`

I changed the current working directory to /challenge/files and then ran the program /challenge/run. We were supposed to conver all files that contained p in 3 characters which is why i used "*p*" which covers all words that start and end with p also having p in the middle. 

```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files/
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{UO7OPRMTqNvbQC1fD2eLEtPlbOi.0lM3kjNxwSN2gjNzEzW}
```

### New Learnings
I learnt how to use multiple globs and how * can even represent nothing so you can make any pattern of your wishing or requirement.

### References 
None. 
