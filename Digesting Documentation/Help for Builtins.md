# Module Name
Digesting Documentation
## Challenge Name
Help for Builtins

Add challenge description here

Some commands are built into the shell itself (builtins). You can list shell builtins with help and get help for a specific builtin with help <name>. This challenge’s challenge command is a builtin; use help to learn the correct --secret value to get the flag.

### Solve
**Flag:** `pwn.college{0OQHd9NYfl78jPkpQ9Bz8CjPpqK.QX0ETO0wiMzEzNzEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
hacker@man~help-for-builtins:~$ help
GNU bash, version 5.2.37(1)-release (x86_64-pc-linux-gnu)
These shell commands are defined internally.  Type `help' to see this list.
Type `help name' to find out more about the function `name'.
Use `info bash' to find out more about the shell in general.
Use `man -k' or `info' to find out more about commands not in this list.

A star (*) next to a name means that the command is disabled.

 job_spec [&]                                                            history [-c] [-d offset] [n] or history -anrw [filename] or history >
 (( expression ))                                                        if COMMANDS; then COMMANDS; [ elif COMMANDS; then COMMANDS; ]... [ e>
 . filename [arguments]                                                  jobs [-lnprs] [jobspec ...] or jobs -x command [args]
 :                                                                       kill [-s sigspec | -n signum | -sigspec] pid | jobspec ... or kill ->
 [ arg... ]                                                              let arg [arg ...]
 [[ expression ]]                                                        local [option] name[=value] ...
 alias [-p] [name[=value] ... ]                                          logout [n]
 bg [job_spec ...]                                                       mapfile [-d delim] [-n count] [-O origin] [-s count] [-t] [-u fd] [->
 bind [-lpsvPSVX] [-m keymap] [-f filename] [-q name] [-u name] [-r ke>  popd [-n] [+N | -N]
 break [n]                                                               printf [-v var] format [arguments]
 builtin [shell-builtin [arg ...]]                                       pushd [-n] [+N | -N | dir]
 caller [expr]                                                           pwd [-LP]
 case WORD in [PATTERN [| PATTERN]...) COMMANDS ;;]... esac              read [-ers] [-a array] [-d delim] [-i text] [-n nchars] [-N nchars] >
 cd [-L|[-P [-e]] [-@]] [dir]                                            readarray [-d delim] [-n count] [-O origin] [-s count] [-t] [-u fd] >
 challenge [--fortune] [--version] [--secret SECRET]                     readonly [-aAf] [name[=value] ...] or readonly -p
 command [-pVv] command [arg ...]                                        return [n]
 compgen [-abcdefgjksuv] [-o option] [-A action] [-G globpat] [-W word>  select NAME [in WORDS ... ;] do COMMANDS; done
 complete [-abcdefgjksuv] [-pr] [-DEI] [-o option] [-A action] [-G glo>  set [-abefhkmnptuvxBCEHPT] [-o option-name] [--] [-] [arg ...]
 compopt [-o|+o option] [-DEI] [name ...]                                shift [n]
 continue [n]                                                            shopt [-pqsu] [-o] [optname ...]
 coproc [NAME] command [redirections]                                    source filename [arguments]
 declare [-aAfFgiIlnrtux] [name[=value] ...] or declare -p [-aAfFilnrt>  suspend [-f]
 dirs [-clpv] [+N] [-N]                                                  test [expr]
 disown [-h] [-ar] [jobspec ... | pid ...]                               time [-p] pipeline
 echo [-neE] [arg ...]                                                   times
 enable [-a] [-dnps] [-f filename] [name ...]                            trap [-lp] [[arg] signal_spec ...]
 eval [arg ...]                                                          true
 exec [-cl] [-a name] [command [argument ...]] [redirection ...]         type [-afptP] name [name ...]
 exit [n]                                                                typeset [-aAfFgiIlnrtux] name[=value] ... or typeset -p [-aAfFilnrtu>
 export [-fn] [name[=value] ...] or export -p                            ulimit [-SHabcdefiklmnpqrstuvxPRT] [limit]
 false                                                                   umask [-p] [-S] [mode]
 fc [-e ename] [-lnr] [first] [last] or fc -s [pat=rep] [command]        unalias [-a] name [name ...]
 fg [job_spec]                                                           unset [-f] [-v] [-n] [name ...]
 for NAME [in WORDS ... ] ; do COMMANDS; done                            until COMMANDS; do COMMANDS-2; done
 for (( exp1; exp2; exp3 )); do COMMANDS; done                           variables - Names and meanings of some shell variables
 function name { COMMANDS ; } or name () { COMMANDS ; }                  wait [-fn] [-p var] [id ...]
 getopts optstring name [arg ...]                                        while COMMANDS; do COMMANDS-2; done
 hash [-lr] [-p pathname] [-dt] [name ...]                               { COMMANDS ; }
 help [-dms] [pattern ...]
hacker@man~help-for-builtins:~$ challenge [--fortune] [--version] [--secret SECRET]
Incorrect usage! Please read the help page for the challenge builtin!
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "0OQHd9NY".
hacker@man~help-for-builtins:~$ challenge --secret 0OQHd9NY
Correct! Here is your flag!
pwn.college{0OQHd9NYfl78jPkpQ9Bz8CjPpqK.QX0ETO0wiMzEzNzEzW}
```

### New Learnings
Help provides a list of shell builtins; help <builtin> displays a builtin's arguments and usage.

 Because builtins run inside the shell rather than using an external executable, man / --help might not be applicable.

 Before attempting to treat a mysterious command like an external program, determine whether it is a built-in command (use type <name> or help).

### References 
Add any references or videos you used while solving the challenge.
