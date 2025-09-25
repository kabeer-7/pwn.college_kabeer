# File Globbing

## Exclusionary GLobbing
We are supposed to run all the files that don't start with a p,w or n. 

### Solve
**Flag:** `pwn.college{MZALBGnNa77OuaciTKc8q1b7Xzc.QX2IDO0wSN2gjNzEzW}`

I changed the current working directory to /challenge/files. We were required to run all the files that did not start with p,w or n, so I entered '/challenge/run [!pwn]*' which makes sure that the files starting with p,w or n are not listed. The * after [!pwn] matches all the files after p,w or n. This completes the challenge and gives me the required flag. 

```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files/
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{MZALBGnNa77OuaciTKc8q1b7Xzc.QX2IDO0wSN2gjNzEzW}
```

### New Learnings
We learn about exclusionary globbing which does the opposite of what we were using globbing to do. Till now, we were using globbing to list or run files that contained certain keywords or characters but here we do the opposite, using ! or ^ at the start of [] we list the files that don't contain certain characters that would be entered into [!]. This type of globbing is used only for [].  

### References 
None. 
