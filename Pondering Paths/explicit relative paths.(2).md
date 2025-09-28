# Module Name
Pondering Paths
## Challenge Name
explicit relative paths.from/

Add challenge description here

Previously, your relative path was "naked": it directly specified the directory to descend into from the current directory. In this level, we're going to explore more explicit relative paths.

In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: . and ... The first, ., refers to the current directory, so these absolute paths are identical:
```bash
/challenge
/challenge/.
/challenge/./././././././././
/./././challenge/././
```
And these relative paths are also identical (when your cwd is /):
```bash
challenge
./challenge
./././challenge
challenge/.
```
This challenge asks you to use . in your relative path when invoking the run program from the root directory (/). In short: change to / and run the program using a relative path that contains .

### Solve
**Flag:** `pwn.college{0JFVSJ9uwSTgbGwW4wwsTkIvu8u.QXwUTN0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{0JFVSJ9uwSTgbGwW4wwsTkIvu8u.QXwUTN0wiMzEzNzEzW}

```

### New Learnings
refers to the current directory; even when it resolves to the same file as an absolute path, adding it to a path (./challenge/run, for example) creates a relative path.

 Paths that begin with / are absolute, while those that do not (even if they begin with.) are relative to cwd.

 Although /,./challenge/run and /challenge/run point to the same file, the program may determine whether your cwd is correct and how it was invoked.

### References 
Add any references or videos you used while solving the challenge.
