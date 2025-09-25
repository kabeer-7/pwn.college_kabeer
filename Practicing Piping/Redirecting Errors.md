# Practising Piping

## Redirecting Errors
We are supposed to redirect the output of /challenge/run to myflag and 'errors' should get redirected to instructions. 

### Solve
**Flag:** `pwn.college{wenxuwUqP4tMeWEAG-4V2YkUa4W.QX3YTN0wSN2gjNzEzW}`

I enter '/challenge/run > myflag 2> instructions' in which > means channel 1 i.e, output that is redirected to myflag and 2> i.e, error gets redirected to instructions. 

```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat instructions 
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ cat myflag 

[FLAG] Here is your flag:
[FLAG] pwn.college{wenxuwUqP4tMeWEAG-4V2YkUa4W.QX3YTN0wSN2gjNzEzW}
```

### New Learnings
I learnt about the file descriptor numbers which describes the communication channel in Linux. FD 0: Standard Input, FD 1: Standard Output and FD 2: Standard Error. With this file descriptor number you can specify the channel that the output, error gets redirected to. So, I learnt how to apply the file descriptor numbers to change the redirection channels. 

### References 
None. 
