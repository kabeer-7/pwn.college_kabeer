# Chaining commands

## Scripting with arguments
We are supposed to create a shell script which takes two arguments and outputs them in the reverse order and then run /challenge/run to get the flag. 

### Solve
**Flag:** `pwn.college{4NQu0JYPV5h6dy6J-ZGp3yHmdke.0VNzMDOxwSN2gjNzEzW}`

I first added the shebang to the script and added the echo statement which prints the second argument before the second argument. Hence, on executing the shell script, the arguments are reversed. Then, on running /challenge/run I get the flag. 

```bash
hacker@chaining~scripting-with-arguments:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ echo 'echo "$2 $1"' >> /home/hacker/solve.sh 
hacker@chaining~scripting-with-arguments:~$ bash /home/hacker/solve.sh hello world
world hello
hacker@chaining~scripting-with-arguments:~$ /challenge/run 
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{4NQu0JYPV5h6dy6J-ZGp3yHmdke.0VNzMDOxwSN2gjNzEzW}
```

### New Learnings
Learnt how to use arguments with bash and understood how they get saved as variables with the first argument being $1 and so on. 

### References 
None. 
