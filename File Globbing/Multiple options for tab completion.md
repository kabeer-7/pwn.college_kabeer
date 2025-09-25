# File Globbing

## multiple options for tab completion
This challenge has a /challenge/files directory with a bunch of files starting with pwncollege. We are supposed to tab-complete from /challenge/files/p to reach the flag. 

### Solve
**Flag:** `pwn.college{4P7wVsJwOcW09oTGGo1ZGiN90lp.0lN0EzNxwSN2gjNzEzW}`

I entered cat /challenge/files/p and hit tab which auto-completed it to pwn, and on hitting tab another time it gave the options for expansion. On doing pwnc and hitting tab it auto-completed to pwncollege and then I further hit tab to see options and then finally entered pwncollege-flag to get the flag. 

```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter  
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking     
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{4P7wVsJwOcW09oTGGo1ZGiN90lp.0lN0EzNxwSN2gjNzEzW}
```

### New Learnings
Learnt how to see all the possible available options for tab completion. 

### References 
None. 
