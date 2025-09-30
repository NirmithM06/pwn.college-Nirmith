# Module Name
Comprehending Commands
## Challenge Name
listing files

Add challenge description here

So far, we've been told which files to interact with. Directories can contain many files (and subdirectories), and you won't always be told their names — so you need to list directory contents with the ls command.

ls lists files in directories provided as arguments, or in the current directory when no arguments are given. In this challenge, the /challenge/run program has been renamed to a random filename. List the files in /challenge to find the executable and run it.

### Solve
**Flag:** `pwn.college{AdurmDhseb571FBr8qE3QR5TcEV.QX4IDO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@commands~listing-files:~$ ls /challenge
32444-renamed-run-4944  DESCRIPTION.md
hacker@commands~listing-files:~$ ls /challenge/32444-renamed-run-4944
/challenge/32444-renamed-run-4944
hacker@commands~listing-files:~$ /challenge/32444-renamed-run-4944
Yahaha, you found me! Here is your flag:
pwn.college{AdurmDhseb571FBr8qE3QR5TcEV.QX4IDO0wiMzEzNzEzW}

```

### New Learnings
To find unknown filenames in directories, use ls.

If you receive "No such file or directory," relist the directory. Don't trust stale filenames.

Once you know the filename, it's easy to run an executable by absolute path.
### References 
Add any references or videos you used while solving the challenge.
