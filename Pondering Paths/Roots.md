# Module Name
Pondering Paths   
## Challenge Name
The Root

### Solve
**Flag:** `pwn.college{UZ3eCksR1iGMAt1xuqESqs6VEmY.QX4cTO0wiMzEzNzEzW}  `

The filesystem you are dropped into has / as its root.  Directly in / is a program called pwn, which, when called, will print the flag.  Running that program with its absolute path (i.e., /pwn) is the aim.  In this environment, running pwn (without a leading /) will not run the same binary; instead, you must reference the executable from the filesystem root.

```bash
hacker@paths~the-root:~$ /
bash: /: Is a directory

hacker@paths~the-root:~$ pwn
It looks like you invoked 'pwn' instead of the absolute path ('/pwn'). You'll 
learn more about how this is different later, but suffice it to say: you ran 
the wrong thing. Use the absolute path, instead!

hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{UZ3eCksR1iGMAt1xuqESqs6VEmY.QX4cTO0wiMzEzNzEzW}

```

### New Learnings
There is a distinct and useful distinction between relative or PATH-based invocations (./pwn or pwn) and absolute invocations (/pwn).

When attempting to run /, the shell displays "Is a directory" instead of executing directories.

Provide the leading / to target files at the filesystem root explicitly when a challenge suggests absolute paths.

### References 
Add any references or videos you used while solving the challenge.
