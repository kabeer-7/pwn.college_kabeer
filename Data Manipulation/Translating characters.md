# Data manipulation

## Translating characters
We are supposed to switch lowercase and uppercase letters to get the flag. 

### Solve
**Flag:** `pwn.college{sXLXCjJbOFkHc154wdmR9J8tDEX.01MxEzNxwSN2gjNzEzW}`

I basically translated all the lowercase to upppercase and viceversa using the ranges of the alphabets. Using tr 'A-Za-z' 'a-zA-Z' would mean convertin A-Z to a-z and a-z to A-Z.  

```bash
hacker@data~translating-characters:~$ /challenge/run | tr 'A-Za-z' 'a-zA-Z'
yOUR CASE-SWAPPED FLAG:
pwn.college{sXLXCjJbOFkHc154wdmR9J8tDEX.01MxEzNxwSN2gjNzEzW}
```

### New Learnings
I learnt how we can use the tr program to translate specific characters by modifying it while piping. 

### References 
Used google to understand how ranges can be applied to tr function. 
