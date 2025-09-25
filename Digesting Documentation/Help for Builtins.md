# Digesting Documentation

## Help for Builtins
We use help to look for information on the challenge builtin and then use the relevant arguments to obtain the flag. 

### Solve
**Flag:** `pwn.college{4-M9fNdHGxDnTfyngidOPj2nopD.QX0ETO0wSN2gjNzEzW}`

Executed help on the challenge builtin to get info about challenge. It gave me the argument to obtain the flag which required a secret value and gave the secret value as well. So, on running 'challenge --secret 4-M9fNdH' I got the required flag. 

```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "4-M9fNdH".
hacker@man~help-for-builtins:~$ challenge --secret 4-M9fNdH
Correct! Here is your flag!
pwn.college{4-M9fNdHGxDnTfyngidOPj2nopD.QX0ETO0wSN2gjNzEzW}
```

### New Learnings
We learn about builtins that are commands built into the shell itself and aren't stored in files. They are faster as the shell runs them internally and doesn't have to search or go through files to run them. They don't have a standard man page as they're built into the shell so we use the help command to read the man page for a specific builtin. On entering help without an argument, we can see a list of all the builtin that the shell supports and using help with an argument of a specific command, we can see it's man page. 


### References 
None. 
