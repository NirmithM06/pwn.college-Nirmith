# Module Name
Pondering Paths
## Challenge Name
Position yet elsewhere

Add challenge description here

The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:
```bash
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the current working directory of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt - it shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!

### Solve
**Flag:** `pwn.college{oZX039yaoLfY1aJretpr_2E0qIS.QX4QTN0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /var directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /var
hacker@paths~position-yet-elsewhere:/var$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{oZX039yaoLfY1aJretpr_2E0qIS.QX4QTN0wiMzEzNzEzW}
hacker@paths~position-yet-elsewhere:/var$ 

```

### New Learnings
When a program specifically looks for the current working directory, it must be changed using cd.

 Certain programs need both the correct working directory and the correct invocation path, but absolute paths and current working directory are two different ideas.

 When program error messages specify a necessary path, take them literally as helpful hints.

### References 
Add any references or videos you used while solving the challenge.
