# Comprehending Commands

## Linking Files
The flag is in /flag but the program /challenge/catflag reads out /home/hacker/not-the-flag. We must use links so that the program reads the file with the flag 

### Solve
**Flag:** `pwn.college{gdQNeAKYK12uHJZRYp41tzARXXT.QX5ETN1wSN2gjNzEzW}`

Since, the program /challenge/catflag only reads out /home/hacker/not-the-flag, I created a symbolic link with not-the-flag which made it linked to /flag. Hence when I run /challenge/catflag, it reads not-the-flag which links it to the /flag file hence giving me the flag. 

```bash
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag 
hacker@commands~linking-files:~$ /challenge/catflag 
About to read out the /home/hacker/not-the-flag file!
pwn.college{gdQNeAKYK12uHJZRYp41tzARXXT.QX5ETN1wSN2gjNzEzW}
```

### New Learnings
Symbolic links are basically something that point to anothe file similar to shortcuts. I learnt about their applications and how they can be used. 

### References 
Used google to understand symbolic links a bit better. 
