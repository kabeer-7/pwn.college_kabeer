# Pondering Path

## Finding Commands
The win command and the flag are in the same directory. We must use the which command to find the directory and then just cat the flag. 

### Solve
**Flag:** `pwn.college{UFdH6kMY4BUexP_SuQsAYEbdAty.01NzEzNxwSN2gjNzEzW}`

I used which to find the directory of the win command and then since the flag is in the same directory, used cat to read the flag. 

```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/6289/win
hacker@path~finding-commands:~$ cat /challenge/paths/6289/flag
pwn.college{UFdH6kMY4BUexP_SuQsAYEbdAty.01NzEzNxwSN2gjNzEzW}
```

### New Learnings
learnt about the which command which is used to find the directory of a command basically telling us where it's located. 

### References 
None. 
