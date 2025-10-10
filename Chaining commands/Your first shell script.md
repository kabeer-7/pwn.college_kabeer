# Chaining commands

## Your first shell script
We are supposed run /challenge/pwn and /challenge/college in a shell script x.sh. 

### Solve
**Flag:** `pwn.college{8xg54ykSEi-VJ0v9Z2gQIvgoSYr.QXxcDO0wSN2gjNzEzW}`

I used echo to add the programs in the shell script and then ran the shell script using bash. Running the shell script ran the two programs and hence gave me the flag. 

```bash
hacker@chaining~your-first-shell-script:~$ echo '/challenge/pwn ; /challenge/college' > x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh 
Great job, you've written your first shell script! Here is the flag:
pwn.college{8xg54ykSEi-VJ0v9Z2gQIvgoSYr.QXxcDO0wSN2gjNzEzW}
```

### New Learnings
Learnt how to make a shell script, add to it and then execute it using bash. 

### References 
Used google to undersand how to make a shell script. 
