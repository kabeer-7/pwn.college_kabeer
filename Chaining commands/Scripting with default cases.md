# Chaining commands

## Scripting with default cases
Add challenge description here

### Solve
**Flag:** `pwn.college{0lg6xTfYtcKosTRj_twFaz8ZSxC.01NzMDOxwSN2gjNzEzW}`

Same as the previous challenge. Just added the else conditional which would print 'nope' if anything other than 'pwn' was given as argument to bash. 

```bash
hacker@chaining~scripting-with-default-cases:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'if [ "$1" = "pwn" ]' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'then' >> /home/hacker/solve.sh 
hacker@chaining~scripting-with-default-cases:~$ echo '    echo "college"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'else' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo '    echo "nope"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ echo 'fi' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ chmod u+x /home/hacker/solve.sh
hacker@chaining~scripting-with-default-cases:~$ /challenge/run 
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{0lg6xTfYtcKosTRj_twFaz8ZSxC.01NzMDOxwSN2gjNzEzW}
```

### New Learnings
Learnt the syntax of else in command line. 

### References 
None. 
