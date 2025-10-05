# Processes and jobs

## Killing processes
We are supposed to find a process called dont_run and kill it as /challenge/run won't run as long as /challenge/dont_run is running. 

### Solve
**Flag:** `pwn.college{ovzeJ7fbfVoZ-9JDMU0PAYEDo0i.QXyQDO0wSN2gjNzEzW}`

I first piped ps -ef to grep for dont_run which gave me the process that I needed to kill (136). After killing the process, I was able to run /challenge/run and got the flag. 

```bash
hacker@processes~killing-processes:~$ ps -ef | grep dont_run
hacker       136     135  0 14:29 ?        00:00:00 /challenge/dont_run
hacker       185     145  0 14:31 pts/0    00:00:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{ovzeJ7fbfVoZ-9JDMU0PAYEDo0i.QXyQDO0wSN2gjNzEzW}
```

### New Learnings
I learnt about how to kill process using 'kill'.

### References 
None. 
