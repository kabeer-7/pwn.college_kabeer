# Hello Hackers

## Command History
The challenge helps us to learn about how to access the command history using up and down arrow.

### Solve
**Flag:** `pwn.college{8fCWIFeUyNRZiLkVLlYpzwQoGm1.0lNzEzNxwSN2gjNzEzW}`

The challenge injected the flag into our command history and we are to obtain it using the functions for checking the command history. So, knowing that command history is checked by using the up and down arrow keys, when the arrow key is pressed we can see the last command which is the necessary flag.

```bash
hacker@hello~command-history:~$ the flag is pwn.college{8fCWIFeUyNRZiLkVLlYpzwQoGm1.0lNzEzNxwSN2gjNzEzW}
```

### New Learnings
I learnt how to scroll through saved commands which are essentially the commands that you inputed previously which get saved. We use up/down arrow keys to scroll through the saved commands. The history contains a log of the commands that we've run. 

### References 
Nothing additional. 
