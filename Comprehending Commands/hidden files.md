# Module Name
Comprehending Commands
## Challenge Name
hidden files

Add challenge description here

Linux hides files whose names begin with . from casual ls output. Use ls -a (or ls -la) to reveal these dot‑prefixed files. This challenge hides the flag file as a dot‑prefixed file directly in / (the filesystem root). Your task is to discover that hidden filename and read its contents.

### Solve
**Flag:** `pwn.college{MMADvA82JQm-cZAN0rf78fyArpX.QXwUDO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash

hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv           bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-2298237461120  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ file /.flag-2298237461120
/.flag-2298237461120: ASCII text
hacker@commands~hidden-files:~$ cat /.flag-2298237461120
pwn.college{MMADvA82JQm-cZAN0rf78fyArpX.QXwUDO0wiMzEzNzEzW}

```

### New Learnings
In many CLI listings, files that start with. are hidden; ls -a or ls -la reveals them.

In CTF-style environments, hidden files may hold crucial information and can reside anywhere in the filesystem, including /.

Before using cat (or head) to read small text files, use file to verify the type if you're not sure.

### References 
Add any references or videos you used while solving the challenge.
