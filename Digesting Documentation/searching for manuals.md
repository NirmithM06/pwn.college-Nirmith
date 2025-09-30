# Module Name
Digesting Documentation
## Challenge Name
searching for manuals

Add challenge description here

This level hides the manpage by randomizing its name. Use the man database search tools (man -k / apropos or man -K) to find the hidden manpage, read it to learn the secret option, then run /challenge/challenge with that option to get the flag.

### Solve
**Flag:** `pwn.college{stimXwEIeBNN7t55p9yL5IHyab7.QX2EDO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
stimwetpyy (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man -k flag
dpkg-buildflags (1)  - returns build flags to use during package build
Dpkg::BuildFlags (3perl) - query build flags
fegetexceptflag (3)  - floating-point rounding and exception handling
fesetexceptflag (3)  - floating-point rounding and exception handling
i386 (8)             - change reported architecture in new program environment and/or set personality flags
ioctl_iflags (2)     - ioctl() operations for inode flags
linux32 (1)          - change reported architecture in new program environment and/or set personality flags
linux64 (1)          - change reported architecture in new program environment and/or set personality flags
pcap-config (1)      - write libpcap compiler and linker flags to standard output
security_compute_av_flags (3) - query the SELinux policy database in the kernel
security_compute_av_flags_raw (3) - query the SELinux policy database in the kernel
set_matchpathcon_flags (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity ...
set_matchpathcon_invalidcon (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of vali...
set_matchpathcon_printf (3) - set flags controlling the operation of matchpathcon or matchpathcon_index and configure the behaviour of validity...
setarch (1)          - change reported architecture in new program environment and/or set personality flags
setarch (8)          - change reported architecture in new program environment and/or set personality flags
stimwetpyy (1)       - print the flag!
x86_64 (8)           - change reported architecture in new program environment and/or set personality flags
hacker@man~searching-for-manuals:~$ man stimwetpyy
hacker@man~searching-for-manuals:~$ 
hacker@man~searching-for-manuals:~$ /challenge/challenge --stimwe 755
Correct usage! Your flag: pwn.college{stimXwEIeBNN7t55p9yL5IHyab7.QX2EDO0wiMzEzNzEzW}
```

### New Learnings
When manpage filenames are indexed but randomized, man -k <term> (also known as apropos <term>) is the best option for quickly searching the manpage index.

 If index search is insufficient, man -K <term> can search the full text of all manpages (slower).

 Inside man, search with /pattern, navigate matches with n/N, and exit with q.

 The man database is strong; even with filenames that aren't human-friendly, you can locate documents.

### References 
Add any references or videos you used while solving the challenge.
