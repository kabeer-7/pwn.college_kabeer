# Pondering PATH

## Adding commands
make a shell script called win, add its location to the PATH, and enable /challenge/run to find it!

### Solve
**Flag:** `pwn.college{oPldhscS98G6TZQhQMPynEZ1HEF.QX2cjM1wSN2gjNzEzW}`

I wrote a shell script and changes the permission for the user to execute it. I then exported the PATH variable for both the current directory and the path of the PATH variable. 

```bash
hacker@path~adding-commands:~$ echo "cat /flag" > win
hacker@path~adding-commands:~$ chmod +x win
hacker@path~adding-commands:~$ export PATH="$(pwd):$PATH"
hacker@path~adding-commands:~$ /challenge/run 
Invoking 'win'....
pwn.college{oPldhscS98G6TZQhQMPynEZ1HEF.QX2cjM1wSN2gjNzEzW}
```

### New Learnings
we can add custom commands to the PATH list

### References 
None. 
