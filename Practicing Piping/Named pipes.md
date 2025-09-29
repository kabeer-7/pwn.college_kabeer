# Practicing Piping

## Named pipes
We need to create a /tmp/flag_fifo file and redirect the stdout of /challenge/run. On doing so, /challenge/run will write the flag into the FIFO. 

### Solve
**Flag:** `pwn.college{gtQnneMdDZvOO_bK7KZOeHVryn6.01MzMDOxwSN2gjNzEzW}`

I create the FIFO /tmp/flag_fifo and then redirect the output of /challenge/run to the FIFO. Due to the blocking feature of FIFO, the writing part is blocked until the content from the FIFO is read. So, I open another terminal and run cat /tmp/flag_fifo which gives me the flag. 

```bash
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo 
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo! 
Bash will now try to open the FIFO for writing, to pass it as the stdout of 
/challenge/run. Recall that operations on FIFOs will *block* until both the 
read side and the write side is open, so /challenge/run will not actually be 
launched until you start reading from the FIFO!
//NEW TERMINAL WINDOW
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo 
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{gtQnneMdDZvOO_bK7KZOeHVryn6.01MzMDOxwSN2gjNzEzW}
```

### New Learnings
Learnt about creating FIFOs using the mkfifo command and about its properties. Learnt about how to add to the fifo and to read it. 

### References 
None. 
