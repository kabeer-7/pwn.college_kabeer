# Comprehending Commands

## Comparing Files
We are given two files in the challenge directory. One file contains a 100 fake flags and the other contains a 100 fake flags plus the real flag. We are required to find the real flag using the diff command. 

### Solve
**Flag:** ` pwn.college{s-d1Hz8UhNrnszpEmf9f3KfTqZx.01MwMDOxwSN2gjNzEzW}`

We've been given that one file contains a 100 fake flags and the other contains a 100 fake flags plus the real flag under the challenge directory (so i switch to the current working directory to /challenge). The diff function is used to find the differene between two files and then it seems obvious that the difference between the two files would be the real flag. Hence, I enter diff with the file names as arguments to obtain the real flag. 

```bash
hacker@commands~comparing-files:~$ cd /challenge
hacker@commands~comparing-files:/challenge$ diff decoys_only.txt decoys_and_real.txt 
53a54
> pwn.college{s-d1Hz8UhNrnszpEmf9f3KfTqZx.01MwMDOxwSN2gjNzEzW}
```

### New Learnings
I learnt the application of the diff command. The diff command is extremely valuable as it compares two files line by line and tells us the difference between them. I also understood how the difference between the two files would be displayed as output. For example, in this challenge, the output is given as 53a54 which means after line 53 of file 1 add line 54 of file 2. 

### References 
None.
