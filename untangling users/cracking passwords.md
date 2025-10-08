# Untangling users 

## Cracking passwords
We have to crack the password in /challenge/shadow-leak and switch user to zardus and execute /challenge/run

### Solve
**Flag:** `pwn.college{c8uadz5NOPOPBc0nqrWzd37MMKl.QX3UDN1wSN2gjNzEzW}`

I first used john the ripper to crack the password. Zardus's password was at the end i.e, aardvark. I then used su with zardus as argument to switch users and entered the password. I then simply ran /challenge/run to get the flag. 

```bash
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak 
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:06 72% 1/3 0g/s 302.4p/s 302.4c/s 302.4C/s 1999991..z9999961
0g 0:00:00:11 0% 2/3 0g/s 307.5p/s 307.5c/s 307.5C/s brenda..keith
0g 0:00:00:13 0% 2/3 0g/s 310.4p/s 310.4c/s 310.4C/s Alexis..bigred
0g 0:00:00:15 0% 2/3 0g/s 309.9p/s 309.9c/s 309.9C/s rockie..surfing
0g 0:00:00:17 1% 2/3 0g/s 311.1p/s 311.1c/s 311.1C/s rosita..help
0g 0:00:00:18 1% 2/3 0g/s 312.3p/s 312.3c/s 312.3C/s nina..Joanna
aardvark         (zardus)
1g 0:00:00:18 100% 2/3 0.05367g/s 312.5p/s 312.5c/s 312.5C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run 
Congratulations, you have become Zardus! Here is your flag:
pwn.college{c8uadz5NOPOPBc0nqrWzd37MMKl.QX3UDN1wSN2gjNzEzW}
```

### New Learnings
Learnt about password hashing and how passwords can be cracked using John the ripper which is an open source tool. Learnt about how passwords are not stored in etc/shadow. Learnt about how the passwords we enter are one way encrypted and matches it against the stored hashed password. 

### References 
Read about john the ripper on google. 
