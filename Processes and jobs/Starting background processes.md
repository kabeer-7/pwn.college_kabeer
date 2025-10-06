# Processes and jobs

## Starting background processes
We are supposed to run /challenge/run in the background directly. 

### Solve
**Flag:** `pwn.college{cN-eLWb5HPzAjDmZw5WTUTGUIym.QX5QDO0wSN2gjNzEzW}`

On entering & after /challenge/run I was able to run /challenge/run in the background from the start. 

```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 161
hacker@processes~starting-backgrounded-processes:~$ 


Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{cN-eLWb5HPzAjDmZw5WTUTGUIym.QX5QDO0wSN2gjNzEzW}

[1]+  Done                    /challenge/run
```

### New Learnings
Learnt how we can start background processes using & without the need to suspend them first and then using bg to resume them in the background. 

### References 
None. 
