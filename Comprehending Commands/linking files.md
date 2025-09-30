# Module Name
Comprehending Commands
## Challenge Name
linking files

Add challenge description here

The challenge expects /challenge/catflag to read /home/hacker/not-the-flag. Create a symbolic link at that path pointing to /flag so the program follows the symlink and reads the real flag.

### Solve
**Flag:** `pwn.college{MC74S7rvc11IQYhLQMKyLqWVZh7.QX5ETN1wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ls -l /home/hacker/not-the-flag
lrwxrwxrwx 1 hacker hacker 5 Sep 30 18:39 /home/hacker/not-the-flag -> /flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{MC74S7rvc11IQYhLQMKyLqWVZh7.QX5ETN1wiMzEzNzEzW}
```

### New Learnings
A symlink linkname → target is created with ln -s target linkname.

Symlinks are displayed as -> with their target when ls -l is used.

Programs can transparently read different files when they open a specific pathname by replacing or creating a symlink.

### References 
Add any references or videos you used while solving the challenge.
