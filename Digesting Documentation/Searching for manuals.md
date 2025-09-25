# Digesting Documentation

## Searching for manuals
We are supposed to go through the man page for man and find the appropriate command to search for the name of the manual which will help us get the flag. 

### Solve
**Flag:** `pwn.college{M3HxDDzaMAwTv8BRo_Ilqum-0td.QX2EDO0wSN2gjNzEzW}`

On going through the man page for man, I found the -k argument (searches for keywords) which seemed appropriate to search for the name of the man page required. On using 'man -k flag' (i used flag as it was highly likely that the man page would contain info related to flag), a man page for xzawvolqum was visible which showed that it prints the flag. On going through this man page, the argument --xzawvo NUM was visible which on giving the number 380 gave the flag.   
```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k flag
dpkg-buildflags (1)  - returns build flags to use during package build
Dpkg::BuildFlags (3perl) - query build flags
fegetexceptflag (3)  - floating-point rounding and exception handling
fesetexceptflag (3)  - floating-point rounding and exception handling
i386 (8)             - change reported architecture in new program environment and/or set personali...
ioctl_iflags (2)     - ioctl() operations for inode flags
linux32 (1)          - change reported architecture in new program environment and/or set personali...
linux64 (1)          - change reported architecture in new program environment and/or set personali...
pcap-config (1)      - write libpcap compiler and linker flags to standard output
security_compute_av_flags (3) - query the SELinux policy database in the kernel
security_compute_av_flags_raw (3) - query the SELinux policy database in the kernel
set_matchpathcon_flags (3) - set flags controlling the operation of matchpathcon or matchpathcon_in...
set_matchpathcon_invalidcon (3) - set flags controlling the operation of matchpathcon or matchpathc...
set_matchpathcon_printf (3) - set flags controlling the operation of matchpathcon or matchpathcon_i...
setarch (1)          - change reported architecture in new program environment and/or set personali...
setarch (8)          - change reported architecture in new program environment and/or set personali...
x86_64 (8)           - change reported architecture in new program environment and/or set personali...
xzawvolqum (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man xzawvolqum
hacker@man~searching-for-manuals:~$ /challenge/challenge  --xzawvo 380
Correct usage! Your flag: pwn.college{M3HxDDzaMAwTv8BRo_Ilqum-0td.QX2EDO0wSN2gjNzEzW}
```

### New Learnings
I learnt how the man page for man can be used to find the man page for the necessary command if the man page is not known. 

### References 
None. 
