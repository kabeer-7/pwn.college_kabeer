# Processes and jobs

## Process exit codes
We are to access the exit code of /challenge/get-code which as an argument to /challenge/submit-code will give the flag. 

### Solve
**Flag:** `pwn.college{o9O_MGPJe8v_wMcsH95bG8PiB1h.QX5YDO1wSN2gjNzEzW}`

I first ran the process /challenge.get-code which gave an error. On entering echo $? where $ is used to access the value of the variable ? which is the varibale for the exit code of the last terminated process. This gave me the exit code for the first process which on using as the argument for the second process gave me the flag. 

```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code 
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
204
hacker@processes~process-exit-codes:~$ /challenge/submit-code 204
CORRECT! Here is your flag:
pwn.college{o9O_MGPJe8v_wMcsH95bG8PiB1h.QX5YDO1wSN2gjNzEzW}
```

### New Learnings
I learnt that exit codes of the last terminated program are stored in the variable ? and this variable can be read using various methods to access the exit code. 

### References 
None. 
