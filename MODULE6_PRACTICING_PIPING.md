# MODULE6_PRACTICING_PIPING

# 1. REDIRECTING OUTPUT

The challenge introduced using `>` to redirect standard output to files using echo.

## My Solve

**Flag:** `pwn.college{EzggNG3QcHtvQCijigqIxuaT67Q.QX0YTN0wSNxAzNzEzW}`

In the problem statement, it was provided that output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase) would yield the flag.
``` 
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{EzggNG3QcHtvQCijigqIxuaT67Q.QX0YTN0wSNxAzNzEzW}
``` 
## What I learned

Learned how to redirect standard output using `>` to write to files.

## References

The problem statement provided was used as the reference.

# 2. REDIRECTING PROGRAM OUTPUT TO A FILE

The challenge introduced redirecting output of any command.

## My Solve

**Flag:** `pwn.college{IINuy6tF-xo3FmNDhYbFe72gNLV.QX1YTN0wSNxAzNzEzW}`

In the problem statement, it was provided that redirecting `/challenge/run` into `myflag` would yield the flag.
```
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
...
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{IINuy6tF-xo3FmNDhYbFe72gNLV.QX1YTN0wSNxAzNzEzW}
```

## What I learned

Learned to redirect output of commands using `>`.

## References

The problem statement provided was used as the reference.

# 3. APPENDING OUTPUT 

The challenge introduced `>>` to append stdout instead of truncating.

## My Solve

**Flag:** `pwn.college{wQGBJGRu9tgmlvhF0t093flF-2G.QX3ATO0wSNxAzNzEzW}`

In the problem statement, it was provided that properly redirecting in append-mode, the second half would appended to the first instead of overwriting in truncation mode (>) and yield the flag.
```
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag
...
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
|
|/ This is the first half:
v
pwn.college{wQGBJGRu9tgmlvhF0t093flF-2G.QX3ATO0wSNxAzNzEzW}
^
that is the second half /|\
```

## What I learned

Learned that `>>` appends to existing files, preserving previous content.

## References

The problem statement provided was used as the reference.

# 4. REDIRECTING ERRORS

The challenge introduced `2>` to redirect standard error to a file.

## My Solve

**Flag:** `pwn.college{0wIl0MK8xs6UIh0-bHVqz7JhElu.QX3YTN0wSNxAzNzEzW}`

In the problem statement, it was provided that the output of /challenge/run, like before, to myflag, and the "errors" to instructions successfully would yield the flag in myflag.
```
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{0wIl0MK8xs6UIh0-bHVqz7JhElu.QX3YTN0wSNxAzNzEzW}
```

## What I learned

Learned to redirect standard error using `2>` separately from stdout.

## References

The problem statement provided was used as the reference.

# 5. REDIRECTING INPUT

The challenge introduced `<` to redirect a file into stdin.

## My Solve

**Flag:** `pwn.college{EdwriJSTcWjaqoug8OsLrGcXcFM.QXwcTN0wSNxAzNzEzW}`

In the problem statement, it was provided that redirecting `COLLEGE` into `/challenge/run` would read the value and yield the flag.
```
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{EdwriJSTcWjaqoug8OsLrGcXcFM.QXwcTN0wSNxAzNzEzW}
```

## What I learned

Learned to redirect file contents using `<`.

## References

The problem statement provided was used as the reference.

# 6. GREPPING STORED RESULTS

The challenge introduced saving output to a file and then using `grep`.

## My Solve

**Flag:** `pwn.college{kGhXK_rmibS310muRN_jWFfPvkT.QX4EDO0wSNxAzNzEzW}`
```
In the problem statement, it was provided that redirecting `/challenge/run` to `/tmp/data.txt` and then  using `grep` would reveal the flag.

hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
...
hacker@piping~grepping-stored-results:~$ grep pwn /tmp/data.txt
pwns
pwn
pwned
pwning
pwn.college{kGhXK_rmibS310muRN_jWFfPvkT.QX4EDO0wSNxAzNzEzW}
```

## What I learned

Learned to combine output redirection with `grep` to search saved results.

## References

The problem statement provided was used as the reference.

# 7. GREPPING LIVE OUTPUT

The challenge introduced using `|` to pipe stdout into another command.

## My Solve

**Flag:** `pwn.college{8ZQwabsXZ408a8owZVfR8e3td-y.QX5EDO0wSNxAzNzEzW}`

In the problem statement, it was provided that /challenge/run will output the flag file upon using grep. 
```
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn
...
[PASS] You have passed the checks on the process on the other end of my stdout!
pwned
pwning
pwn.college{8ZQwabsXZ408a8owZVfR8e3td-y.QX5EDO0wSNxAzNzEzW}
pwn
pwns
```

## What I learned

Learned to use `|` to directly pipe command output into another command.

## References

The problem statement provided was used as the reference.

# 8. GREPPING ERRORS

The challenge introduced combining `2>&1` with `|` to grep through stderr.

## My Solve

**Flag:** `pwn.college{kASb_DS-T10A7KTXbJ_zKhLUq_c.QX1ATO0wSNxAzNzEzW}`

In the problem statement, it was provided that redirecting errors and using `grep` would yield the flag.
```
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.college
...
[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{kASb_DS-T10A7KTXbJ_zKhLUq_c.QX1ATO0wSNxAzNzEzW}
```

## What I learned

Learned to merge stderr into stdout using `2>&1` before piping.

## References

The problem statement provided was used as the reference.

# 9. FILTERING WITH GREP -v

The challenge introduced using `grep -v` to filter out unwanted lines.

## My Solve

**Flag:** `pwn.college{MkwjNGmoENpG1i4buVnVxqkStYk.0FOxEzNxwSNxAzNzEzW}`

In the problem statement, it was provided that using grep -v to filter out all the lines containing "DECOY" would reveal the real flag.
```
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{MkwjNGmoENpG1i4buVnVxqkStYk.0FOxEzNxwSNxAzNzEzW}
```
## What I learned

Learned to use `grep -v` to invert matches and filter out unwanted lines.

## References

The problem statement provided was used as the reference.


# 10. DUPLICATING PIPED DATA WITH TEE

The challenge introduced using `tee` to intercept piped data.

## My Solve

**Flag:** `pwn.college{Qs4hV49s6nR9wBvN4Cy_3x5O_eL.QXxITO0wSNxAzNzEzW}`

In the problem statement, it was provided that piping /challenge/pwn into /challenge/college and intercepting the data to see what pwn needs would yield the flag.
```
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee intercepted_data | /challenge/college
Processing...
WARNING: you are overwriting file intercepted_data with tee's output...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat intercepted_data
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "Qs4hV49s"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret Qs4hV49s | tee intercepted_data | /challenge/college
Processing...
WARNING: you are overwriting file intercepted_data with tee's output...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{Qs4hV49s6nR9wBvN4Cy_3x5O_eL.QXxITO0wSNxAzNzEzW}
```

## What I learned

Learned to use `tee` to duplicate piped data to both files and commands.

## References

The problem statement provided was used as the reference.

# 11. PROCESS SUBSTITUTION FOR INPUT

The challenge introduced using `<(...)` to treat command output as files.

## My Solve

**Flag:** `pwn.college{AqayF6CWO35zbHKw6WqxVe2ZkjF.0lNwMDOxwSNxAzNzEzW}`

In the problem statement, it was provided that comparing the outputs of `/challenge/print_decoys` and `/challenge/print_decoys_and_flag` with `diff <(...)` would reveal the flag.
```
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
51a52

pwn.college{AqayF6CWO35zbHKw6WqxVe2ZkjF.0lNwMDOxwSNxAzNzEzW}
```

## What I learned

Learned to use process substitution `<(...)` to compare command outputs as files.

## References

The problem statement provided was used as the reference.

# 12. WRITING TO MULTIPLE PROGRAMS

The challenge introduced `>(...)` to write output to commands.

## My Solve

**Flag:** `pwn.college{kQr8F6JRBSOkNrqbP4nEJut29SF.QXwgDN1wSNxAzNzEzW}`

In the problem statement, it was provided that running the /challenge/hack command, and duplicating its output as input to both the /challenge/the and the /challenge/planet commands would yield the flag.
```
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{kQr8F6JRBSOkNrqbP4nEJut29SF.QXwgDN1wSNxAzNzEzW}
```

## What I learned

Learned to use process substitution `>(...)` with `tee` to direct output to multiple commands.

## References

The problem statement provided was used as the reference.

# 13. SPLIT PIPING STDERR AND STDOUT

The challenge introduced splitting stderr and stdout to separate commands.

## My Solve

**Flag:** `pwn.college{k8G7JBEkeSpn3ZK_wfUTpMDi8Ck.QXxQDM2wSNxAzNzEzW}`

In the problem statement, it was provided that redirecting hack's stderr to /challenge/the  and redirecting hack's stdout to /challenge/planet would yield the flag.
```
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{k8G7JBEkeSpn3ZK_wfUTpMDi8Ck.QXxQDM2wSNxAzNzEzW}
```

## What I learned

Learned to split stdout to one command and stderr to another using `>(...)` and `2>`.

## References

The problem statement provided was used as the reference.

# 14. NAMED PIPES 

The challenge introduced creating FIFOs with `mkfifo` and redirecting output to them.

## My Solve

**Flag:** `pwn.college{M2o1y0o5O8e1-Q-9ynfDSI2uc35.01MzMDOxwSNxAzNzEzW}`

In the problem statement, it was provided that creating a /tmp/flag_fifo file and redirecting the stdout of /challenge/run to it would yield the flag when read.
```
TERMINAL1:

hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo

TERMINAL2:

hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of
/challenge/run. Recall that operations on FIFOs will *block* until both the
read side and the write side is open, so /challenge/run will not actually be
launched until you start reading from the FIFO!

TERMINAL1:

You've correctly redirected /challenge/run's stdout to a FIFO at
/tmp/flag_fifo! Here is your flag:
pwn.college{M2o1y0o5O8e1-Q-9ynfDSI2uc35.01MzMDOxwSNxAzNzEzW}
```

## What I learned

Learned to create named pipes with `mkfifo` and redirect output to them for inter-process communication.

## References

The problem statement provided was used as the reference.






