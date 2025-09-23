# Pondering Paths

## Implicit relative path using .
running the program from the /challenge directory by explicitly using relative paths to launch run using '.'. 

### Solve
**Flag:** `pwn.college{gEK-Z3kC_1_LNvebL2i75xKhCp6.QXxUTN0wSN2gjNzEzW}`

I, first, changed the directory to /challenge and then executed './run' which tells the command line to run the 'run' program in the current working directory i.e, '/challenge'. 

```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gEK-Z3kC_1_LNvebL2i75xKhCp6.QXxUTN0wSN2gjNzEzW}

```

### New Learnings
I learnt how to explicitly use relative paths to launch run in this challenge and how we have to tell the linux command line to explicitly execute a program in the current working directory. 

### References 
None. 
