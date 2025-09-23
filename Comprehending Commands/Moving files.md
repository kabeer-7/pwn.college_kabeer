# Comprehending Commands

## Moving Files
This challenge wants you to move the /flag file into /tmp/hack-the-planet. 

### Solve
**Flag:** `pwn.college{k3_28aXKZz5j2AjYfclRSHIip4F.0VOxEzNxwSN2gjNzEzW}`

I used the mv command to move /flag to /tmp/hack-the-planet. Then, running /challenge/check checks if the file has been moved correctly and gives the flag back to me. 

```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{k3_28aXKZz5j2AjYfclRSHIip4F.0VOxEzNxwSN2gjNzEzW}
```

### New Learnings
I learnt how mv command can be used to move and rename files. 'mv' with an argument of a file name renames the file, for example, 'mv old.txt new.txt' changes the file name from old to new. 'mv' with an argument of a path changes the location of the file, for example, 'mv file.txt /new_location' changes the location of the file from home directory to new_location. 

### References 
None. 
