# Module Name
Comprehending Commands
## Challenge Name
grepping for a needle in a haystack

Add challenge description here

Sometimes files are enormous and cat-ing them is not practical. grep searches files for lines containing a pattern and prints matching lines. Invoke it like:
```bash
grep SEARCH_STRING /path/to/file
```
In this challenge a very large file lives at /challenge/data.txt. The flag is somewhere in that file and — as a hint — every flag starts with pwn.college. Use grep to find the flag.

### Solve
**Flag:** `pwn.college{sGEikBfm2xJVOmRvNqh8XjbIvad.QX3EDO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash

grep pwn.college /challenge/data.txt

pwn.college{sGEikBfm2xJVOmRvNqh8XjbIvad.QX3EDO0wiMzEzNzEzW}

```

### New Learnings
The quickest and easiest method for locating text in big files is to use grep.

When regex is not required, use literal patterns or -F for fixed-string searches.

To limit or count matches, combine grep with head, wc, or other utilities.

### References 
Add any references or videos you used while solving the challenge.
