# Module Name
Digesting Documentation
## Challenge Name
Reading Manuals

Add challenge description here

This level introduces the man command. man is short for manual, and will display (if available) the manual of the command you pass as an argument. For example, man yes shows the yes manpage with NAME, SYNOPSIS, DESCRIPTION, and so on. Manpages live under /usr/share/man and you query them by name (man yes, not man /usr/bin/yes).

The challenge has a secret option documented in the challenge manpage; use it to make the program print the flag.

### Solve
**Flag:** `pwn.college{0EF-89_5T098yzfZ3G5J6B9rnSE.QX0EDO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ ls -l /challenge/challenge
file /challenge/challenge
/challenge/challenge --yzfrnw 089 2>&1 | sed -n '1,200p'
-rws--x--x 1 root root 636 Jan 14  2025 /challenge/challenge
/challenge/challenge: setuid executable, regular file, no read permission
Correct usage! Your flag: pwn.college{0EF-89_5T098yzfZ3G5J6B9rnSE.QX0EDO0wiMzEzNzEzW}
```

### New Learnings
To find the right argument forms and available options, use man <command>.

 Standard sections (NAME, SYNOPSIS, DESCRIPTION) on manpages typically include a list of the precise option names and necessary argument formats.

 Be mindful of formatting (leading zeros, hex, etc.) for commands that take numeric arguments; manpages will frequently outline the required format.

 Although they can be used to check a binary's permissions and properties, ls -l and file are not a replacement for reading the documentation.

### References 
Add any references or videos you used while solving the challenge.
