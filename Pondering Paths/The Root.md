# Pondering Paths

## The root
The challenge requires us to invoke a program by providing its path on the command line. A pwn program was added which upon running will provide us with the flag. 

### Solve
**Flag:** `pwn.college{kHRnQlyI7VBudc1tvLYod9OLUo4.QX4cTO0wSN2gjNzEzW}`

We are supposed to run the pwn program which was added. It's location is right after / which is where the filesystem starts. So, upon providing the path on the command line i.e, '/pwn'. On providing the path, we get the required flag. 

```bash
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{kHRnQlyI7VBudc1tvLYod9OLUo4.QX4cTO0wSN2gjNzEzW}
```

### New Learnings
The filesystem starts at / and then several directories, files, programs and flags are filed after this. We learn about all these components. Directories function just as folders which contain subdirectories and files. Files contain content like source code and programs refer to the source code. I also learnt how to run a given program. 

### References 
Referred to AI to understand terms.
