# Practising piping

## writing to multiple programs
The challenge asked us to run the /challenge/hack command and duplicate its output as input to the commands /challenge/the and /challenge/planet. 

### Solve
**Flag:** `pwn.college{gDZfO_k6DLQP5A1cWb4thYSwOvt.QXwgDN1wSN2gjNzEzW}`

I piped the main program i.e, /challenge/hack to 'tee >(/challenge/the)' which took the output from the program as input to the program here and tee copied it further to the next pipe. The output was then also inputted to the /challenge/planet command. This gave me the flag. 

```bash
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) | >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and 
/challenge/planet. Don't try to copy-paste it; it changes too fast.
4873215252614715630
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{gDZfO_k6DLQP5A1cWb4thYSwOvt.QXwgDN1wSN2gjNzEzW}

```

### New Learnings
I learnt about >(command) which is extremely useful as it enables us to use a file as an input to a command. It is another application of process substitution. 

### References 
None. 
