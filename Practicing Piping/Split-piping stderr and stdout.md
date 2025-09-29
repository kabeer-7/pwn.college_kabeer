# Practicing Piping

## Split-piping stderr and stdout
We are supposed to pipe the output and error of /challenge/hack to /challenge/planet and /challenge/the respectively. 

### Solve
**Flag:** `pwn.college{0tUdkJxaEKVXFrbm0mWYx2_aWcP.QXxQDM2wSN2gjNzEzW}`

Using | and tee with 2>&1 would not work as it would either duplicate only output or only error so it struck me that we would have to use > to redirect the output to a temporary file and >(command) would read the file as input to the command. So, you can find below what I entered to obtain the required flag. 
```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts 
struggle with! Here is your flag:
pwn.college{0tUdkJxaEKVXFrbm0mWYx2_aWcP.QXxQDM2wSN2gjNzEzW}

```

### New Learnings
I learnt how to logically apply the different commands and processes to do what is asked of us. 

### References 
None. 
