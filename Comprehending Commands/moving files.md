# Module Name
Comprehending Commands
## Challenge Name
moving files

Add challenge description here

mv moves (or renames) files and directories. In this challenge the goal is to move the system flag file from its current location to /tmp/hack-the-planet. After moving the flag, run the provided checker (/challenge/check) to verify the move and receive the flag.

### Solve
**Flag:** `pwn.college{Ud-gDN3CCwptGpPTEL8Dn-iAaJF.0VOxEzNxwiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@commands~moving-files:~$ ls
b
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
\Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/run
bash: /challenge/run: No such file or directory
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{Ud-gDN3CCwptGpPTEL8Dn-iAaJF.0VOxEzNxwiMzEzNzEzW}

```

### New Learnings
Moving files between directories or renaming them is possible with mv; it doesn't require reading the contents of the file.

Depending on the environment and permissions, moving a file may still be possible even if you encounter permission errors when attempting to read it (Permission denied).

Always pay close attention to the challenge output because the environment frequently prints hints and confirmations (such as the Correct! Performing... line).

### References 
Add any references or videos you used while solving the challenge.
