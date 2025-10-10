# Chaining commands

## Scripting with conditionals
For this challenge, write a script at /home/hacker/solve.sh that: Takes one argument; If the argument is "pwn", output "college"; For any other input, output nothing

### Solve
**Flag:** `pwn.college{8OBaq68iU_0gh-Y77dajXUIn3vY.0lNzMDOxwSN2gjNzEzW}`

The challenge given to us is extremely similar to the example. I entered the lines of a simple conditional code to the shell script after adding the shebang. The conditional was made such that the terminal will output 'college' if the bash recieves 'pwn' as the argument. I then changed the file permissions for the shell and ran /challenge/run to check. This gave me the flag.

```bash
hacker@chaining~scripting-with-conditionals:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'if [ "$1" = "pwn" ]' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'then' >> /home/hacker/solve.sh 
hacker@chaining~scripting-with-conditionals:~$ echo '    echo "college"' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ echo 'fi' >> /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ chmod u+x /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{8OBaq68iU_0gh-Y77dajXUIn3vY.0lNzMDOxwSN2gjNzEzW}
```

### New Learnings
Learnt the syntax of conditional statements in linux shells and how they can be used. 

### References 
None. 
