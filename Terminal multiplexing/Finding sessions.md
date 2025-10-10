# Terminal Multiplexing 

## Finding sessions 
We are given 3 sessions which we're supposed to connect to and find the flag (which is in one session) by trial and error. 

### Solve
**Flag:** `pwn.college{helloworld}`

I used 'screen -ls' to see the available sessions and then connected to each one using 'screen -r session_name'. On connecting to the right session, I got the flag. 

```bash
command 1
command 2
pwn.college{helloworld}
```

### New Learnings
Learnt how to find sesdions and list them out using screen -ls. We can then connect to specific sessions using 'screen -r session_name'. 

### References 
None. 