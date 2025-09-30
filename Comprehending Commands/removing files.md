# Module Name
Comprehending Commands
## Challenge Name
removing files

Add challenge description here

Files accumulate and need cleanup. This level creates a delete_me file in your home directory. You must remove it with rm and then run /challenge/check — the checker will verify the file is gone and, if so, print the flag.

### Solve
**Flag:** `pwn.college{EAkReK-nPKfYhA5UhSa6kd8M1OX.QX2kDM1wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@commands~removing-files:~$ ls
b  delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/run
bash: /challenge/run: No such file or directory
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{EAkReK-nPKfYhA5UhSa6kd8M1OX.QX2kDM1wiMzEzNzEzW}
```

### New Learnings
Files are removed by rm; ls allows you to verify their presence or absence.

 To prevent inadvertent deletion, always verify the path twice before deleting files.

 Certain challenge binaries check the filesystem state (whether files are present or not) and only continue if certain requirements are fulfilled.

### References 
Add any references or videos you used while solving the challenge.
