# Practising Piping

## Filtering with grep -v
We are supposed to use grep -v to filter out the decoy flags present in the program /challenge/run

### Solve
**Flag:** `pwn.college{EWn2Qqeb4IQQP1I5BZ1BRd9CVBg.0FOxEzNxwSN2gjNzEzW}`

I piped the output from /challenge/run and used grep -v to filter out DECOY which gave me the flag required. 

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{EWn2Qqeb4IQQP1I5BZ1BRd9CVBg.0FOxEzNxwSN2gjNzEzW}
```

### New Learnings
Learnt about grep -v which does the opposite of grep and removes the keyword from the output or search. 

### References 
none
