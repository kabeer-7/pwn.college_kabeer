# Digeseting Documentation

## Learning from documentation
We are asked to invoke the /challenge/challenge program using --giveflag which has been provided as documentation. 

### Solve
**Flag:** `pwn.college{cMdJpJ5HMOdNEMybrPQKO1miNv4.QX0ITO0wSN2gjNzEzW}`

We've been directly told that the argument required to run /challenge/challenge program is --giveflag. Hence, I execute '/challenge/challenge --giveflag'. The argument with the program gives me the required flag. 

```bash
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{cMdJpJ5HMOdNEMybrPQKO1miNv4.QX0ITO0wSN2gjNzEzW}
```

### New Learnings
We learn about documentation and how it helps us understand how the program is needed to be run. This challenge helped me understand that every program has a specific type of argument that should be passed to it to obtain the necessary output. Each program is used differently, and in this case to run the /challenge/challenge we needed --giveflag, similar to how we execute ls with -a to view all the hidden files in a directory. The information about using --giveflag to run the program was part of the documentation associated with the program.  

### References 
None. 
