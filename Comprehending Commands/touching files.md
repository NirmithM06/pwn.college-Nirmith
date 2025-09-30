# Module Name
Comprehending Commands
## Challenge Name
touching files

Add challenge description here

You can create new, empty files quickly using touch. In this level you must create two files — /tmp/pwn and /tmp/college — and then run the challenge program to receive the flag.

### Solve
**Flag:** `pwn.college{Io6GyufaoAEMO29E7K5qBQ8RGvT.QXwMDO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
cd /tmp
touch pwn
touch college
/challenge/run
Success! Here is your flag:
pwn.college{Io6GyufaoAEMO29E7K5qBQ8RGvT.QXwMDO0wiMzEzNzEzW}

```

### New Learnings
Touch can quickly create the files a program might look for by creating empty files or updating timestamps.

 Short-lived files benefit from temporary directories like /tmp, which are frequently used in scripts or challenges.

 In order to gate progress, many challenge programs check for the existence of files (and occasionally their contents or permissions).

### References 
Add any references or videos you used while solving the challenge.
