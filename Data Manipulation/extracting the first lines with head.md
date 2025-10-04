# Data manipulation

## Extracting the first lines with head
We are supposed to extract the first 7 lines from /challenge/pwn and thenn further pipe it to /challenge/college to get the flag. 

### Solve
**Flag:** `pwn.college{UOTqt8CEO8xCC5uLTZBKHWtf9gf.0lNxEzNxwSN2gjNzEzW}`

I piped /challenge/pwn to head -n 7 which reads the first line of code and then i further piped the output i.e, the first 7 lines of code to /challenge/college hence giving me the flag. 

```bash
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college 
Congratulations, you piped the right codes!
pwn.college{UOTqt8CEO8xCC5uLTZBKHWtf9gf.0lNxEzNxwSN2gjNzEzW}
```

### New Learnings
I learnt about the head function which is used to read the first few lines of a program. Without specifiying, it reads the first 10 but the number of lines can be specified using head -n.

### References 
Nonw. 
