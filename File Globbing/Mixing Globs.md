# File Globbing

## Mixing Globs
We are given diversified files in /challenge/files and we are to run /challenge/run. We are supposed to glob such that we cover all arguments matching files "challenging", "educational", and "pwning". 

### Solve
**Flag:** `pwn.college{QRa6V4MlIBOPIYZuSOTB6CkG0hp.QX1IDO0wSN2gjNzEzW}`

I changed the current working directory to /challenge/files. I had initally tried running challenge/run [cep] which did not work the way I wanted as [] only cover single given charactes. Upon correction, I added * which made sure that the pattern is matched after the intial letters and covered all 3 files. Doing so, gave me the required flag. 
```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files/
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{QRa6V4MlIBOPIYZuSOTB6CkG0hp.QX1IDO0wSN2gjNzEzW}
```

### New Learnings
I learnt how to use logic to deduct how to cover all files by mixing multiple globs hence saving us time. 

### References 
None. 
