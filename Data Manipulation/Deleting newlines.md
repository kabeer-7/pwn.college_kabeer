# Data manipulation

## Deleting newlines
A bunch of newlines have been injected into the flag. We must delete these newlines and obtain the fla.g

### Solve
**Flag:** `pwn.college{M0iLIEe1U9OI0o6xCEXjk3OK64A.0VNxEzNxwSN2gjNzEzW}`

I enter the command tr -d '\n' which is used to delete all newline characters from text. 

```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d '\n'
Your line-split flag: pwn.college{M0iLIEe1U9OI0o6xCEXjk3OK64A.0VNxEzNxwSN2gjNzEzW}
```

### New Learnings
I learnt about how to delete newlines. Understood about how \n is a standin for newline and when on entering tr -d '\n', we delete all newline characters from the text.

### References 
None
