# Module Name
Pondering Paths
## Challenge Name
Position thy self

Add challenge description here
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument:

```bash
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the current working directory of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out- that's the directory cd changes. The prompt's ~ shows the current path your shell is located at.

This challenge requires you to execute the /challenge/run program from a specific path (the program will tell you which). You must cd into that directory, then re-run the challenge program. Good luck!

### Solve
**Flag:** `pwn.college{Q2s5PvEbOiPBALAu8zCih1OLkKw.QX2QTN0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@paths~position-thy-self:~$ cd
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /var/log directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /var/log
hacker@paths~position-thy-self:/var/log$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Q2s5PvEbOiPBALAu8zCih1OLkKw.QX2QTN0wiMzEzNzEzW}
hacker@paths~position-thy-self:/var/log$ 

```

### New Learnings
The distinction between a program's internal checks regarding the current working directory and calling it by absolute path.

 How to change the shell's current working directory with cd (and how the prompt reflects that).

 The ability of challenge programs to enforce the absolute path (the way they are called) and the working directory (the place they are called from).

### References 
Add any references or videos you used while solving the challenge.
