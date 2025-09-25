# Digesting Documentation

## Helpful programmes
The challenege asks us to read the documentation of a program using --help instead of man pages to obtain the way to get the flag. 

### Solve
**Flag:** `pwn.college{cLhIbCTFZ7ijifYlufxUK5_fCSe.QX3IDO0wSN2gjNzEzW}`

I used --help on the program /challenge/challenge to read it's documentation. The documenation listed out the -g argument which would print the value that will case the -g option to give me the flag. So, I got the value 753 and then on executing 753 as argument to -g like this: '/challenge/challenge -g 753', I obtained the flag. 

```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 753
hacker@man~helpful-programs:~$ /challenge/challenge -g 753
Correct usage! Your flag: pwn.college{cLhIbCTFZ7ijifYlufxUK5_fCSe.QX3IDO0wSN2gjNzEzW}
```

### New Learnings
Learnt of alternative ways to read the documentation of a program i.e, --help, -h, -?, help or even /?. 

### References 
None. 
