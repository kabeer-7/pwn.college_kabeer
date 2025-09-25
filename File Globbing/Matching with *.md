# File Globbing

## Matching with *
We are to change the current working directory to /challenge using * and not using more than four characters as argument to cd and then run /challenge/run. 

### Solve
**Flag:** `pwn.college{cOameC1AqCxPxsyUY3JaJ33_0r-.QXxIDO0wSN2gjNzEzW}`

I entered cd /c*/ which makes up for four characters as argument to cd. This changed my current working directory to /challenge. I was then able to run the /challenge/run program with the same logic using *. 

```bash
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /c*/
hacker@globbing~matching-with-:/challenge$ /c*/r*
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{cOameC1AqCxPxsyUY3JaJ33_0r-.QXxIDO0wSN2gjNzEzW}
```

### New Learnings
I learnt about globbing which is a method to shorten the way we write paths and expands the commands to match files. In this challenge, we learn about '*'. * matches all the patterns possible before the command is executed. For example, if we use cd *.txt, it'll match all files ending with .txt. Or if we use echo file*, it will print out all the files which start with 'file'. 

### References 
Used AI to understand * better. 
