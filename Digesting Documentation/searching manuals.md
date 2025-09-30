# Module Name
Digesting Documentation
## Challenge Name
searching manuals

Add challenge description here

You can scroll man pages with the arrow keys (and PgUp/PgDn) and search with /. After searching, hit n to go to the next result and N to go to the previous. Use ? to search backwards. Find the option that will give you the flag by reading the challenge man page


### Solve
**Flag:** `pwn.college{QoC1BDPKu4DNuq1GGnAMBw4IJKo.QX1EDO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@man~searching-manuals:~$ man challenge

gzip: stdout: Broken pipe
hacker@man~searching-manuals:~$ /challenge/challenge --vgp
Initializing...
Correct usage! Your flag: pwn.college{QoC1BDPKu4DNuq1GGnAMBw4IJKo.QX1EDO0wiMzEzNzEzW}
```

### New Learnings
To search the manpage, use / inside man; to cycle matches, use n/N; and to search backwards, use?

 It is possible to pipe or filter man output; gzip:  Stdout: When leaving the pager early, a broken pipe is not dangerous.

 Reading manpages is frequently the quickest way to find hidden or unique flags for challenge binaries, as they are the authoritative source for available options.

### References 
Add any references or videos you used while solving the challenge.
