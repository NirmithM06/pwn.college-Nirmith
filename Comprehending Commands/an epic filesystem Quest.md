# Module Name
Comprehending Commands
## Challenge Name
an epic filesystem Quest

Add challenge description here

ou start at / and must follow a chain of breadcrumbs (files named like HINT/BRIEF/CLUE, etc.) using only basic filesystem tools (ls, cat, cd) to locate a hidden flag. Some clues may be protected (e.g., “trapped” if you cd into a directory) — pay attention to what each hint warns you about.

### Solve
**Flag:** `pwn.college{g3VfMg567v_iWeimW2wWr5yVvh3.QX5IDO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls -a/opt/linux/linux-5.4/include/config/generic/strncpy/from
ls: invalid option -- '/'
Try 'ls --help' for more information.
hacker@commands~an-epic-filesystem-quest:/$ ls -a /opt/linux/linux-5.4/include/config/generic/strncpy/from
.  ..  CUE-TRAPPED  user.h
hacker@commands~an-epic-filesystem-quest:/$ cat /opt/linux/linux-5.4/include/config/generic/strncpy/from/CUE-TRAPPED
Lucky listing!
The next clue is in: /usr/share/racket/collects/file

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/$ ls -a /usr/share/racket/collects/file
.   TRACE-TRAPPED  compiled         glob.rkt    gzip.rkt  md5.rkt  resource.rkt  tar.rkt    untgz.rkt  zip.rkt
..  cache.rkt      convertible.rkt  gunzip.rkt  ico.rkt   private  sha1.rkt      untar.rkt  unzip.rkt
hacker@commands~an-epic-filesystem-quest:/$ cat /usr/share/racket/collects/file/TRACE-TRAPPED
Tubular find!
The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Gyre-Pagella/Marks

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Gyre-Pagella/Marks
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Gyre-Pagella/Marks$ ls -a
.  ..  MESSAGE  Regular
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Gyre-Pagella/Marks$ file MESSAGE
MESSAGE: ASCII text
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Gyre-Pagella/Marks$ cat MESSAGE
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/arch/sparc/net

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/Gyre-Pagella/Marks$ cd
hacker@commands~an-epic-filesystem-quest:~$ ls -a /opt/linux/linux-5.4/arch/sparc/net
.  ..  MEMO-TRAPPED  Makefile  bpf_jit_32.h  bpf_jit_64.h  bpf_jit_asm_32.S  bpf_jit_comp_32.c  bpf_jit_comp_64.c
hacker@commands~an-epic-filesystem-quest:~$ cat /opt/linux/linux-5.4/arch/sparc/net/MEMO-TRAPPED
Congratulations, you found the clue!
The next clue is in: /usr/local/lib/python3.8/dist-packages/itanium_demangler-1.1.dist-info
hacker@commands~an-epic-filesystem-quest:~$ ls -a /usr/local/lib/python3.8/dist-packages/itanium_demangler-1.1.dist-info
.  ..  INSTALLER  LEAD  LICENSE-0BSD.txt  METADATA  RECORD  WHEEL  top_level.txt
hacker@commands~an-epic-filesystem-quest:~$ file top_level.txt
top_level.txt: cannot open `top_level.txt' (No such file or directory)
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/local/lib/python3.8/dist-packages/itanium_demangler-1.1.dist-info/top_level.txt
itanium_demangler
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/local/lib/python3.8/dist-packages/itanium_demangler-1.1.dist-info/LEAD
Great sleuthing!
The next clue is in: /usr/local/lib/python3.8/dist-packages/angr/angrdb

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:~$ cd /usr/local/lib/python3.8/dist-packages/angr/angrdb
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/angrdb$ ls -a
.  ..  ALERT  __init__.py  __pycache__  db.py  models.py  serializers
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/angrdb$ ls
ALERT  __init__.py  __pycache__  db.py  models.py  serializers
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/angrdb$ file ALERT
ALERT: ASCII text
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/angrdb$ cat ALERT
Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/scipy/signal/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/angr/angrdb$ cd
hacker@commands~an-epic-filesystem-quest:~$ ls -a /usr/lib/python3/dist-packages/scipy/signal/__pycache__
.                           _max_len_seq.cpython-38.pyc     filter_design.cpython-38.pyc      spectral.cpython-38.pyc
..                          _peak_finding.cpython-38.pyc    fir_filter_design.cpython-38.pyc  waveforms.cpython-38.pyc
.TIP                        _savitzky_golay.cpython-38.pyc  lti_conversion.cpython-38.pyc     wavelets.cpython-38.pyc
__init__.cpython-38.pyc     _upfirdn.cpython-38.pyc         ltisys.cpython-38.pyc
_arraytools.cpython-38.pyc  bsplines.cpython-38.pyc         signaltools.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/lib/python3/dist-packages/scipy/signal/__pycache__/.TIP
Tubular find!
The next clue is in: /usr/share/perl/5.30.0/unicore/lib/Scx

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:~$ ls -a /usr/share/perl/5.30.0/unicore/lib/Scx
.        Armn.pl  Cham.pl  Dupl.pl  Gonm.pl  Han.pl   Hmnp.pl  Knda.pl  Limb.pl  Mult.pl  Rohg.pl  Tagb.pl  Thaa.pl  Zinh.pl
..       Beng.pl  Copt.pl  Ethi.pl  Gran.pl  Hang.pl  Kana.pl  Kthi.pl  Lina.pl  Mymr.pl  Shrd.pl  Takr.pl  Tibt.pl  Zyyy.pl
.HINT    Bhks.pl  Cprt.pl  Geor.pl  Grek.pl  Hebr.pl  Khar.pl  Lana.pl  Linb.pl  Nand.pl  Sind.pl  Talu.pl  Tirh.pl  Zzzz.pl
Adlm.pl  Bopo.pl  Cyrl.pl  Glag.pl  Gujr.pl  Hira.pl  Khmr.pl  Lao.pl   Mlym.pl  Orya.pl  Sinh.pl  Taml.pl  Xsux.pl
Arab.pl  Cakm.pl  Deva.pl  Gong.pl  Guru.pl  Hmng.pl  Khoj.pl  Latn.pl  Mong.pl  Phlp.pl  Syrc.pl  Telu.pl  Yi.pl
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/share/perl/5.30.0/unicore/lib/Scx/.HINT
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{g3VfMg567v_iWeimW2wWr5yVvh3.QX5IDO0wiMzEzNzEzW}
```

### New Learnings
Always carefully read the exact text of the clues; authors occasionally include traps that are activated by cding into a directory.  
(-) Absolute paths (`cat /path/to/file`) or ()`ls /path/to/dir`) allow you to view or read files inside a directory without having to `cd`-in. This prevents adverse effects associated with directory entry.  
(-) To view hidden files and verify permissions before trying to `cat` a file, use `ls -la`.

### References 
Add any references or videos you used while solving the challenge.
