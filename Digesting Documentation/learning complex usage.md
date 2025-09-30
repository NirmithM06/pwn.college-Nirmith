# Module Name
Digesting Documentation
## Challenge Name
learning complex usage

Add challenge description here

This level teaches that some commands take arguments which themselves take arguments (e.g., find -name PATTERN), and gives documentation for /challenge/challenge which prints files when given --printfile <path>.

### Solve
**Flag:** `pwn.college{Q2r4_NXGHEJvY3xm4R9g0rIMboR.QX1ITO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
acker@man~learning-complex-usage:~$ ls -a /challenge/challenge
/challenge/challenge
hacker@man~learning-complex-usage:~$ /challenge/challenge --giveflag
Incorrect usage! You passed the wrong argument (read the challenge description 
for details).
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile
You must pass a file for --printfile to read!
hacker@man~learning-complex-usage:~$ ls -a /challenge
.  ..  .init  DESCRIPTION.md  challenge
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/DECRIPTION.md
Correct argument! Here is the /challenge/DECRIPTION.md file:
cat: /challenge/DECRIPTION.md: No such file or directory
hacker@man~learning-complex-usage:~$ cd /challenge/DECRIPTION.md
bash: cd: /challenge/DECRIPTION.md: No such file or directory
hacker@man~learning-complex-usage:~$ cat /challenge/DECRIPTION.md
cat: /challenge/DECRIPTION.md: No such file or directory
hacker@man~learning-complex-usage:~$ ls -a /challenge
.  ..  .init  DESCRIPTION.md  challenge
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/DESCRIPTION.md
Correct argument! Here is the /challenge/DESCRIPTION.md file:
While using most commands is straightforward, the usage of some commands can get quite complex.
For example, the arguments to commands like `sed` and `awk`, which we're definitely not getting into right now, are entire programs in an esoteric programming language!
Somewhere on the spectrum between `cd` and `awk` are commands that take arguments to their arguments...

This sounds crazy, but you've already encountered this with the `find` level in [Basic Commands](/linux-luminarium/commands).
`find` has a `-name` argument, and the `-name` argument itself takes an argument specifying the name to search for.
Many other commands are analogous.

Here is this level's documentation for `/challenge/challenge`:

> Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The argument to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the description of the level!

Given that documentation, go get the flag!
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{Q2r4_NXGHEJvY3xm4R9g0rIMboR.QX1ITO0wiMzEzNzEzW}
```

### New Learnings
Certain command-line options, like --printfile <path>, take their own arguments.

 Always check filenames for typos (for example, DESCRIPTION.md versus DECRIPTION.md).

 Before gaining access to sensitive targets like /flag, it is advisable to confirm behavior on a secure sample file (such as DESCRIPTION.md).

### References 
Add any references or videos you used while solving the challenge.
