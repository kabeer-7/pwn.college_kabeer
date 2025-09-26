# Shell variables

## Reading Files
We are supposed to read a file into the variable PWN in one line to obtain the flag.

### Solve
**Flag:** `pwn.college{IAhiEOI1vQB77UuBSw-A3WeLptb.QXwIDO0wSN2gjNzEzW}`

I simply used it directly where the file on the right < acts as the input to read and hence sets the value of PWN to the contents of the file. 

```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me 
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{IAhiEOI1vQB77UuBSw-A3WeLptb.QXwIDO0wSN2gjNzEzW}
```

### New Learnings
I learnt about how we can directly input other files into the read command using < instead of using several lines of code with cat command and others. 

### References 
None. 
