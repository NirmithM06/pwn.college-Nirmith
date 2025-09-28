# Module Name
Pondering Paths
## Challenge Name
implicit relative paths, from /

Add challenge description here

Now you're familiar with absolute paths and changing directories. Absolute paths work regardless of your current working directory (cwd), but relative paths depend on the cwd.

A relative path does not start with /.

A relative path is interpreted relative to your current working directory.

Your prompt shows your current working directory.

Example: file at /tmp/a/b/my_file

If cwd is / → relative path tmp/a/b/my_file

If cwd is /tmp → relative path a/b/my_file

If cwd is /tmp/a/b/c → relative path ../my_file (.. = parent directory)

This challenge requires you to run /challenge/run using a relative path while your current working directory is /. The challenge gives a hint: the relative path starts with the letter c.

### Solve
**Flag:** `pwn.college{wDwE71v6HH8-ApbRomn0WPjbXXA.QX5QTN0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{wDwE71v6HH8-ApbRomn0WPjbXXA.QX5QTN0wiMzEzNzEzW}
hacker@paths~implicit-relative-paths-from-:/$ 

```

### New Learnings
The current working directory determines how relative paths are resolved.

 Challenge/run is a relative path from / to /challenge/run.

 Practice using CD and relative versus absolute executable invocation.

### References 
Add any references or videos you used while solving the challenge.
