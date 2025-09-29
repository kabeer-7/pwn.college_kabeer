# Practicing Piping

## Dupicating piped data with tee
We must pipe /challenge/pwn into /challenge/college but we have to see what /challenge/pwn wants first. 

### Solve
**Flag:** `pwn.college{QYmGhaMIjXswNu9omFVhNiF1s1U.QXxITO0wSN2gjNzEzW}`

First, I redirected the output from /challenge/pwn to a random file named okay, on reading okay we got to know that /challenge/pwn should be used with --secret and a secret arugement that was given. I then piped /challenge/pwn with the secret argument into /challenge/college which gave me the correct flag.  

```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee okay | /challenge/college 
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat okay 
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "QYmGhaMI"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret QYmGhaMI | /challenge/college 
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{QYmGhaMIjXswNu9omFVhNiF1s1U.QXxITO0wSN2gjNzEzW}
```

### New Learnings
We have a tee command which is used to duplicated the piped data. When we piped a program, we can't see its data or output, so what the tee command does is, it lets us duplicate the content to a file while piping it further to another program. 

### References 
None.
