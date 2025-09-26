# Practising Piping

## Process substitution for input
We are to use diff command on two set of command outputs which contain a bunch of decoy files. The real flag is the difference between the two command outputs and will get printed. 

### Solve
**Flag:** `pwn.college{gT7fpR_TBhluNmV2ohe0mGGaulM.0lNwMDOxwSN2gjNzEzW}`

Using diff, I printed out the difference amongst the two files using <(command). This gave me the required flag. 

```bash
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
98a99
> pwn.college{gT7fpR_TBhluNmV2ohe0mGGaulM.0lNwMDOxwSN2gjNzEzW}
```

### New Learnings
I learnt about process substitution which basically substitutes the output or input of commands to the argument of another command. This is done using <(command) which creates a temporary file in bash that stores the output of the command. Reading this temporary file will basically be the same as reading the output from the command. 

### References 
None. 
