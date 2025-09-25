# File Globbing

## Matching with []
We are supposed to change the directory to /challenge/files which contains some files. We are to run /challenge/run with all these files as arguments which can be shorted by using []. 

### Solve
**Flag:** `pwn.college{gqglyhxVPQrhZ60ROEixL0ntnuW.QXzIDO0wSN2gjNzEzW}`

I first change the current working directory to /challenge/files. Then I execute '/challenge/run file_[bash]' which then runs the program with all the files_ ending with the letters b, a, s and h individually. This was asked of us and gives us the required flag.  
```bash
hacker@globbing~matching-with-:~$ cd /challenge/files/
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{gqglyhxVPQrhZ60ROEixL0ntnuW.QXzIDO0wSN2gjNzEzW}
```

### New Learnings
I learnt about the file globbing method of []. It works for single characters like in ? but instead of matching any character it only matches the characters given in []. For example, file_[abc] would only match file_a, file_b and file_c and not any file_. 

### References 
None. 
