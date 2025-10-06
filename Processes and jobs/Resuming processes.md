# Processes and jobs

## Resuming processes
We are supposed to suspend a process and then resume it to obtain the flag. 

### Solve
**Flag:** `pwn.college{wyxtDSWD36THdss7-zeODZMxhBv.QX2QDO0wSN2gjNzEzW}`

I ran the /challenge/run process and then suspended it using ctrl+z and resumed it by entering the fg command which gave me the flag. The prompt then told me to press enter to wuit 
```bash
hacker@processes~resuming-processes:~$ /challenge/run 
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{wyxtDSWD36THdss7-zeODZMxhBv.QX2QDO0wSN2gjNzEzW}
Don't forget to press Enter to quit me!

Goodbye!

```

### New Learnings
Learnt that processes can be resumed by using the fg command. 

### References 
None. 
