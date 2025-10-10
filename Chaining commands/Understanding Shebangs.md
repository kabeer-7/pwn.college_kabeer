# Chaining commands

## Understanding Shebangs
We are supposed to make a shell script with the correct Shebang which outputs 'hack the planet'. After this, on running /challenge/run, we will get the flag.

### Solve
**Flag:** `pwn.college{oUi6HIzdz7WDgqt9BN34VR3OST3.0VOzMDOxwSN2gjNzEzW}`

I first created the shell script with the shebang as bash and then appended the echo command to it. I then altered the permissions for the shell script so it could be explicitly run without bash. On running /challenge/run, it verified the challenge and gave me the flag.

```bash
hacker@chaining~understanding-shebangs:~$ echo '#!/bin/bash' > /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ echo 'echo "hack the planet"' >> /home/hacker/solve.sh
hacker@chaining~understanding-shebangs:~$ chmod u+xwr /home/hacker/solve.sh 
hacker@chaining~understanding-shebangs:~$ /challenge/run 
Testing your script...
Perfect! Your flag:
Flag: pwn.college{oUi6HIzdz7WDgqt9BN34VR3OST3.0VOzMDOxwSN2gjNzEzW}
```

### New Learnings
I learnt about shebangs that are the first characters at the start of a script which tells the operating system which interpreter to use.

### References 
None
