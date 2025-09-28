# Module Name
Pondering Paths
## Challenge Name
Program and absolute paths

Add challenge description here


The challenges in pwn.college are located in the challenge directory, which is located directly in the root directory (/), with the exception of the previous level. Thus, /challenge is the path to the challenge directory. This level's challenge program, run, is located in the /challenge directory. Consequently, /challenge/run is the path to the run challenge program.

Once more, you must complete this task by calling upon its absolute path. You should run the file located in the challenge directory, which is located in the / directory. The flag will be awarded to you if you correctly invoke the challenge. Best of luck!

### Solve
**Flag:** `pwn.college{oXZR2k3YLuAWsx8AVJ41F_ziwFG.QX1QTN0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@paths~program-and-absolute-paths:~$ /challenge
bash: /challenge: Is a directory

hacker@paths~program-and-absolute-paths:~$ run
bash: run: command not found

hacker@paths~program-and-absolute-paths:~$ challenge
bash: challenge: command not found

hacker@paths~program-and-absolute-paths:~$ /run
bash: /run: Is a directory

hacker@paths~program-and-absolute-paths:~$ /challenge/rin
bash: /challenge/rin: No such file or directory

hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{oXZR2k3YLuAWsx8AVJ41F_ziwFG.QX1QTN0wiMzEzNzEzW}
hacker@paths~program-and-absolute-paths:~$

```

### New Learnings
emphasized the distinction between command lookup using PATH (run), absolute paths (/challenge/run), and relative paths (./run).

 learned to check if a path is an executable or a directory (helpful hints can be found in shell messages such as "Is a directory" and "command not found").

 Execution will be prevented by minor typos in filenames or paths; when addressing filesystem-based issues, always double-check the precise paths.

### References 
Add any references or videos you used while solving the challenge.
