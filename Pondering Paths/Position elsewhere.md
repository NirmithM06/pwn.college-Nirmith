# Module Name
Pondering Paths
## Challenge Name
Position elsewhere

Add challenge description here

The Linux filesystem has many directories and files. You navigate between directories with the cd (change directory) command:
```bash
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
cd changes the current working directory of your shell (the directory the process is ''i''). The prompt's ~ reflects your current location.

This challenge requires you to execute the /challenge/run program from a specific directory (the program tells you which). You must cd into that directory, then run the program again to get the flag. Good luck!
### Solve
**Flag:** `pwn.college{M2tjbrC7e4J109wOLZg6QyEbciw.QX3QTN0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/share/doc
hacker@paths~position-elsewhere:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{M2tjbrC7e4J109wOLZg6QyEbciw.QX3QTN0wiMzEzNzEzW}
hacker@paths~position-elsewhere:/usr/share/doc$

```

### New Learnings
emphasized the distinction between the current working directory and the invocation path (absolute vs. relative).

 cd modifies the shell's or process's current working directory; some programs verify this and won't work unless they are called from a specific directory.

 Take program output messages literally. For example, "You are not currently in the /usr/share/doc directory."

### References 
Add any references or videos you used while solving the challenge.
