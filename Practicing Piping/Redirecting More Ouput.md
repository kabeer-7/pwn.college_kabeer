# Practising Piping

## Redirecting more output
We are supposed to redirect the output of the /challenge/run program to a file called myflag. 

### Solve
**Flag:** `pwn.college{gQDznGHPVPQBZshbkzEzjh-6z9j.QX1YTN0wSN2gjNzEzW}`

So I entered '/challenge/run > myflag' which redirects the output of the program to the file and then the terminal does it's checks. When on reading the myflag file through cat, I get the desired flag. 

```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{gQDznGHPVPQBZshbkzEzjh-6z9j.QX1YTN0wSN2gjNzEzW}
```

### New Learnings
No futher learning, just redirected the output of another command to a file to read the flag. 

### References 
None.
