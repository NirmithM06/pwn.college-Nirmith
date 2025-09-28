# Module Name
Pondering Paths
## Challenge Name
implicit relative path

Add challenge description here

In this level, we'll practice referring to paths using . a bit more. This challenge needs you to run the program from the /challenge directory.

Linux intentionally avoids automatically searching the current directory when you type a "naked" command name (no / or ./), because doing so would allow accidental execution of programs in the current directory that shadow system utilities. So from /challenge:
```bash
run
```
will not execute /challenge/run — you'll get bash: run: command not found.

To explicitly execute a program in the current directory you must use . (the current directory) in the path. In this level you must cd /challenge and then run the program using a relative path that uses . (for example ./run).

### Solve
**Flag:** `pwn.college{IC9vytjYxVJvjGDwW_svDjfX4fA.QXxUTN0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{IC9vytjYxVJvjGDwW_svDjfX4fA.QXxUTN0wiMzEzNzEzW}
hacker@paths~implicit-relative-path:/challenge$

```

### New Learnings
When you type a bare command name, the shell does not automatically search the current directory for programs; instead, you must specifically use./ to run executables in the cwd.

 The current directory is indicated by. in a path; a local binary can be safely and clearly run with./program.

 An essential Linux safety and tooling concept is comprehending PATH behavior and explicit relative invocation.

### References 
Add any references or videos you used while solving the challenge.
