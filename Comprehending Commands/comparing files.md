# Module Name
Comprehending Commands
## Challenge Name
comparing files

Add challenge description here

When looking for changes between similar files, eyeballing them might not be the most efficient approach — diff helps. diff compares two files line by line and reports what changed (lines added, removed, or modified). In this level you are given two files:

/challenge/decoys_only.txt — contains 100 fake flags

/challenge/decoys_and_real.txt — contains the same 100 fake flags plus the one real flag

Use diff to find the difference between the files and reveal the real flag

### Solve
**Flag:** `pwn.college{YSIrJtdNDh0dwORRtdyzx722IWX.01MwMDOxwiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash

diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt

20a21
> pwn.college{YSIrJtdNDh0dwORRtdyzx722IWX.01MwMDOxwiMzEzNzEzW}

```

### New Learnings
diff shows the exact line-level changes (added, removed, or altered) between two files.

Where and how files differ are indicated by the a/c/d notation in diff output (20a21, for example, means "after line 20 add line 21").

Diff will clearly display the extra lines when one file contains all of the contents of another plus extras, making it ideal for finding a single hidden flag among decoys.

### References 
Add any references or videos you used while solving the challenge.
