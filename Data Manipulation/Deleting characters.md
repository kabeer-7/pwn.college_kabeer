# Data manipulation

## Deleting characters
We are given a flag which contains some decoy characters like ^ and %. We must delete these characters from the flag using tr -d. 

### Solve
**Flag:** `pwn.college{sNnGjC6pUZuuCSIzBsMaZlltUaX.0FNxEzNxwSN2gjNzEzW}`

I used tr -d to delete the characters ^ and % from the flag given by /challenge/run. I used '' which is used when we want to delete multipled characters. 

```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d '^%'
Your character-stuffed flag:
pwn.college{sNnGjC6pUZuuCSIzBsMaZlltUaX.0FNxEzNxwSN2gjNzEzW}
```

### New Learnings
I learnt how characters can be deleted using tr -d and how we can use '' to delete multiple characters. 

### References 
Used google to understand how to delete multiple characters in the same line. 
