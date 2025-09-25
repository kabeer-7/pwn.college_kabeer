# File Globbing

## Matching paths with []
Now we're supposed to run the program from the home directory using [] to match the path of the files. 

### Solve
**Flag:** `pwn.college{wJnuTITN1jwpOpTsh_5_unkiYXQ.QX0IDO0wSN2gjNzEzW}`

I just ran the program similar to the previous challenge, the only difference is that we ran it from the home directory. 

```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{wJnuTITN1jwpOpTsh_5_unkiYXQ.QX0IDO0wSN2gjNzEzW}
```

### New Learnings
No new learning, just used file globbing to match the path instead of the file. 

### References 
None. 
