# Shell variables

## Printing variables
The challenge asks us to print out the FLAG variable. 

### Solve
**Flag:** `pwn.college{QO6f3YQm2j9ZUU5KCnsY12L-vQT.QX3UTN0wSN2gjNzEzW}`

I entered echo $FLAG, since the $ denote that FLAG is a shell variable and this is how echo can be used to print out shell variables. 

```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{QO6f3YQm2j9ZUU5KCnsY12L-vQT.QX3UTN0wSN2gjNzEzW}
```

### New Learnings
We learn about variables and how echo can be used to print shell varibales by prepending the variable name with a $. 

### References 
None. 
