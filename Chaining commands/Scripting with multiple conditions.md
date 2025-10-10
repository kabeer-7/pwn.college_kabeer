# Chaining commands

## Scripting with multiple conditions
For this challenge, write a script at /home/hacker/solve.sh that: Takes one argument; If the argument is "hack", output "the planet"; If the argument is "pwn", output "college"; If the argument is "learn", output "linux"; For any other input, output "unknown"

### Solve
**Flag:** `pwn.college{cXtbaljcxSS1Qk13g0Zvo3NWSyw.0FOzMDOxwSN2gjNzEzW}`

Similar to basic coding conditions, I used the same logic with the same syntax for elif as if and solved it. On running /challenge/run, I got the flag. 

```bash
hacker@chaining~scripting-with-multiple-conditions:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ echo 'if [ "$1" == "hack" ]; then' >> /home/hacker/solve.sh ; echo '    echo "the planet"' >> /home/hacker/solve.sh ; echo 'elif [ "$1" == "pwn" ]; then' >> /home/hacker/solve.sh ; echo '    echo "college"' >> /home/hacker/solve.sh ; echo 'elif [ "$1" == "learn" ]; then' >> /home/hacker/solve.sh ;  echo '    echo "linux"' >> /home/hacker/solve.sh ;  echo 'else' >> /home/hacker/solve.sh ;  echo '    echo "unknown"' >> /home/hacker/solve.sh ; echo 'fi' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-multiple-conditions:~$ chmod u+wxr /home/hacker/solve.sh 
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run 
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{cXtbaljcxSS1Qk13g0Zvo3NWSyw.0FOzMDOxwSN2gjNzEzW}
```

### New Learnings
Just learnt the syntax of elif and how we can use it to script multiple conditionals. 

### References 
None. 
