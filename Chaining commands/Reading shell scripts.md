# Chaining commands

## Reading shell scripts
We are supposed to read the shell script for /challenge/run and then run the program with the secret password to get the flag. 

### Solve
**Flag:** `pwn.college{MA3ZNZSA1HkWt35Xex61DdXDDSQ.0lMwgDOxwSN2gjNzEzW}`

I used cat to read the shell script which indicated that we had to enter a secret password which was 'hack the PLANET'. I then ran the program program which prompted me for a password, which on currectly entering, I got the flag. 

```bash
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run 
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
	echo "CORRECT! Your flag:"
	cat /flag
else
	echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:~$ /challenge/run 
hack the PLANET
CORRECT! Your flag:
pwn.college{MA3ZNZSA1HkWt35Xex61DdXDDSQ.0lMwgDOxwSN2gjNzEzW}
```

### New Learnings
Learnt that cat can be used to read other shell scripts given so that we can understand what a shell script is executing. 

### References 
None. 
