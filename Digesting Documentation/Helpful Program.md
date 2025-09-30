# Module Name
Digesting Documentation
## Challenge Name
Helpful Program

Add challenge description here

Some programs don't have a man page, but might tell you how to run them if invoked with a special argument. Usually this is --help (or -h, etc.). In this level you read a program's built‑in help and use it to get the flag


### Solve
**Flag:** `pwn.college{0KdwoySTX9Tp6_pCcmubWhialOQ.QX3IDO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 96
hacker@man~helpful-programs:~$ /challenge/challenge -g "<96>"
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: '<96>'
hacker@man~helpful-programs:~$  /challenge/challenge --give-the-flag "<96>"
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: '<96>'
hacker@man~helpful-programs:~$ /challenge/challenge -g "< 96>"
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: '< 96>'
hacker@man~helpful-programs:~$ /challenge/challenge -g 96
Correct usage! Your flag: pwn.college{0KdwoySTX9Tp6_pCcmubWhialOQ.QX3IDO0wiMzEzNzEzW}
```

### New Learnings
When a program doesn't have a man page, use --help (or -h), which frequently provides a list of useful options.

 To safely find the correct input for a guarded option, use -p (print the required value).

 Pass the plain number (without <> or extra characters) when a program asks for an integer argument.

 The token printed by the helper option should always be copied and passed verbatim (watch out for accidental punctuation).

### References 
Add any references or videos you used while solving the challenge.
