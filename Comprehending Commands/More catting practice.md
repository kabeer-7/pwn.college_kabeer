# Comprehending Commands

## More catting practice
We have to read the flag file in a complicated directory without entering the directory using cd. 

### Solve
**Flag:** `pwn.college{cILS5VUwpNB0kK4UkEenfnbD8VB.QXwITO0wSN2gjNzEzW}`

I entered the cat command with the given absolute path as the argument to run the flag file which returns the required flag to me. Entering the absolute path as argument goes to the location directly withou the need to use cd to enter the directory. 

```bash
hacker@commands~more-catting-practice:~$ cat /lib/x86_64-linux-gnu/engines-1.1/flag
pwn.college{cILS5VUwpNB0kK4UkEenfnbD8VB.QXwITO0wSN2gjNzEzW}
```

### New Learnings
Nothing new learnt on top of the previous challenge other than accessing more directories to read the required file using cat. 

### References 
None.
