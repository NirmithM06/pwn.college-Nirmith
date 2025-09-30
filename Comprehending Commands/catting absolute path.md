# Module Name
Comprehending Commands
## Challenge Name
catting absolute paths

Add challenge description here

In the previous level you read the flag from your home directory with cat flag. You can also give cat absolute paths — full paths starting with / — and it will print whatever file you point it to. In this level the flag file is left readable at the absolute path /flag. Your job is to read /flag with cat and capture the flag.
### Solve
**Flag:** `pwn.college{cScqv8C4mDU89FjF3LUyYzm-FzW.QX5ETO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{cScqv8C4mDU89FjF3LUyYzm-FzW.QX5ETO0wiMzEzNzEzW}
```

### New Learnings
Absolute paths, which are resolved from the filesystem root and are not dependent on your current working directory, are accepted by cat.

To debug cat failures (missing file, incorrect path, permission denied), use ls -l.

cat is a quick and easy way to examine the contents of a file.
### References 
Add any references or videos you used while solving the challenge.
