# Digesting Documentation

## Reading Manuals
We are supposed to read the manual for challenge to understand how to obtain the flag. 

### Solve
**Flag:** `pwn.college{wQIZNUVATkQnKmtAmBJ7b3IT2Ef.QX0EDO0wSN2gjNzEzW}`

I ran 'man challenge' to get the man page for challenge. On the man page, three options were given out of which only --wknmtm NUM seemed to contain the way to get the flag. It said that 732 instead of NUM would give us the flag. Looking at the syntax in the man page, I entered '/challenge/challene -wknmtm 732' which gave me the required flag. 

```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --wknmtm 732
Correct usage! Your flag: pwn.college{wQIZNUVATkQnKmtAmBJ7b3IT2Ef.QX0EDO0wSN2gjNzEzW}
```

### New Learnings
We learn about man pages which are built-in documentations for commands and programs. They make it easy to gain information about a command or program without needing to access the internet. I also learnt how to read a man page about a specific command and understand what to use from the man page to obtain the required flag. 

### References 
Used google to understand how to read man pages better. 
