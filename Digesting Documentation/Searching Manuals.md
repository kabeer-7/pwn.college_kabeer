# Digesting Documentation

## Searching Manuals
We are supposed to search the man page to find the argument which would give us the flag. 

### Solve
**Flag:** `pwn.college{cyc6gpVEtWFHfOeAm0MwTStwXPo.QX1EDO0wSN2gjNzEzW}`

I first entered man challenge to see the man page for challenge. Then using / I searched for anything that said flag and kept going through the searches by entering 'n'. Eventually, I found the argument which gave the flag (--wllwapv) when used along with the /challenge/challenge command. 

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --wllwapv
Initializing...
Correct usage! Your flag: pwn.college{cyc6gpVEtWFHfOeAm0MwTStwXPo.QX1EDO0wSN2gjNzEzW}
```

### New Learnings
I learnt how to search for certain things in a man page. We can use / to search up keywords from the start of the man page or ? to search from the back. We can go to the next result using 'n' and to the previous result using 'N'. 

### References 
None. 
