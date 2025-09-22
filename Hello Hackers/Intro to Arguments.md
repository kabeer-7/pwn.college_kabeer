# Hello Hackers

## Intro to Arguments
The challenge asks us to invoke and execute the 'echo' and 'hello' commands with the argument of 'hackers'. 

### Solve
**Flag:** `pwn.college{wYRQ8xOmkgJw_NAZersbJBieOy4.QX4YjM1wSN2gjNzEzW}`

We invoke the hello command with the argument of 'hackers'. The hello command with the argument hackers satisfies the parameters given and hence we obtain the required flag. 

```bash
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{wYRQ8xOmkgJw_NAZersbJBieOy4.QX4YjM1wSN2gjNzEzW}
```

### New Learnings
In this challenge, we learn about commands with arguments. The first word is the command and the words after are the arguments to the specific command, in this case 'echo' and 'hello'. The 'echo' command gives us the arguments as output. So, when we enter 'echo hello hackers', we get the output of 'hello hackers'. The echo command is similar to the print command. Arguments can be altered. 


### References 
None. 
