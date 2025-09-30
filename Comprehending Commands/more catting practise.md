# Module Name
Comprehending Commands
## Challenge Name
more catting practise

Add challenge description here

You can specify all sorts of paths as arguments to commands, and we'll practice some more with cat. In this level, the flag is placed in a non‑standard directory and you are not allowed to change directories with cd. You must retrieve the flag by absolute path from wherever you are.

The challenge hint tells you the flag location: /lib/bash/flag. Read it with cat without using cd.

### Solve
**Flag:** `pwn.college{QNp5JVcrB2-THiJnd_5EdZAb5IF.QXwITO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
# confirm we cannot cd (challenge forbids it) — not strictly necessary, but illustrative
# (Attempting cd would be blocked in the challenge environment; we skip cd.)

# Read the flag directly by absolute path
cat /lib/bash/flag

# Expected output
pwn.college{QNp5JVcrB2-THiJnd_5EdZAb5IF.QXwITO0wiMzEzNzEzW}

```

### New Learnings
Without altering your current working directory, absolute paths let you access files from anywhere on the filesystem.

A quick tool for reading files with absolute paths is called cat.

In order to make you learn and rely on absolute paths and path inspection tools, some challenge levels purposefully limit CD.

### References 
Add any references or videos you used while solving the challenge.
