# Comprehending Commands

## Grepping for a needle in a haystack
We need to invoke the grep command to find the flag amongst a hundred thousand lines of code in a file. 

### Solve
**Flag:** `pwn.college{w_UnN5tsr8qq_t1uvDuMIHssNKH.QX3EDO0wSN2gjNzEzW}`

The hint given was that every flag starts with pwn.college and we had to obtain the flag from amongst a hundred thousand lines of code in /challenge/data.txt. The grep command contains the basic syntax: 'grep SEARCH_STRING /path/to/file'. In this case, using the hint given the search_string would be pwn.college as the grep command searches the file for any code containing the particular search string. 

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{w_UnN5tsr8qq_t1uvDuMIHssNKH.QX3EDO0wSN2gjNzEzW}

```

### New Learnings
I learnt how to use the grep command and it's syntax. It is useful as it can help search text or patterns within files. 

### References 
None.
