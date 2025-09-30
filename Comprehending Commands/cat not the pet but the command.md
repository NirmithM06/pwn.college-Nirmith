# Module Name
Comprehending Commands
## Challenge Name
cat: not the pet, but the command!

Add challenge description here

One of the most critical Linux commands is cat. cat is most often used for reading files (and concatenating multiple files when several arguments are provided). In this challenge the system copies the flag into a file named flag in your home directory. Your job is simply to read that file with cat and capture the flag.

### Solve
**Flag:** `pwn.college{ATGWMqPl8FE2MdcCB56y2aNEHBd.QXxcTN0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{ATGWMqPl8FE2MdcCB56y2aNEHBd.QXxcTN0wiMzEzNzEzW}
hacker@commands~cat-not-the-pet-but-the-command:~$ 

```

### New Learnings
A basic command for rapidly reading file contents from the terminal is cat.

 Your home directory is indicated by the shell prompt ~; a lot of challenge files, such as flag, are stored there.

 Before trying to read a file, ls -la and ls -l are helpful diagnostics when unsure of the file names or permissions.

### References 
Add any references or videos you used while solving the challenge.
