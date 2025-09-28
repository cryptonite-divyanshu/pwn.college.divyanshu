# MODULE5_FILE_GLOBBING

# 1. MATCHING WITH *

The challenge resets working directory to /home/hacker unless directory is changed properly. It introduced globbing with `*` to match directory names.

## My Solve

**Flag:** `pwn.college{QKNaxHUEcLUvpQZ_Rtltj1lr4BZ.QXxIDO0wSNxAzNzEzW}`

In the problem statement, it was provided that changing into `/challenge` using '*' to keep characters to 4 and then running the program would yield the flag.
```
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{QKNaxHUEcLUvpQZ_Rtltj1lr4BZ.QXxIDO0wSNxAzNzEzW}
```

## What I learned

Learned to use the `*` wildcard to match prefixes in directory names.

## References

The problem statement provided was used as the reference.

# 2. MATCHING WITH ?

The challenge introduced `?` to match single characters in directory names.

## My Solve

**Flag:** `pwn.college{8OFph6gVe7pO84dLD5XD6GZqTyj.QXyIDO0wSNxAzNzEzW}`

In the problem statement, it was provided that changing into `/challenge` using '?' to avoid characters 'c' and 'l' and then running the program would yield the flag.

```
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8OFph6gVe7pO84dLD5XD6GZqTyj.QXyIDO0wSNxAzNzEzW}
```

## What I learned

Learned to use the `?` wildcard to match exactly one character in path names.

## References

The problem statement provided was used as the reference.

# 3. MATCHING WITH []

The challenge required matching filenames using bracket expressions to specify character sets.

## My Solve

**Flag:** `pwn.college{Exebww9X4e3lHdZfUpV9fbaLBKY.QXzIDO0wSNxAzNzEzW}`

In the problem statement, it was provided that changing working directory to /challenge/files and running /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h would yield the flag.
```
hacker@globbing~matching-paths-with-:~$ cd /challenge/files
hacker@globbing~matching-paths-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{Exebww9X4e3lHdZfUpV9fbaLBKY.QXzIDO0wSNxAzNzEzW}
```

## What I learned

Learned to use bracket expressions `[ ]` to match specific sets of characters in filenames.

## References

The problem statement provided was used as the reference.

# 4. MATCHING PATHS WITH []

The challenge resets working directory to /home/hacker unless directory is changed properly. It introduced matching paths with [].

## My Solve

**Flag:** `pwn.college{AXZosfoqkI0Z5VBbDJLay7leA6I.QX0IDO0wSNxAzNzEzW}`

In the problem statement, it was provided that starting from home directory and running /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files would yield the flag.

```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{AXZosfoqkI0Z5VBbDJLay7leA6I.QX0IDO0wSNxAzNzEzW}
```
## What I learned

Learned that globbing works with full paths as well as relative patterns.

## References

The problem statement provided was used as the reference.

# 5. MULTIPLE GLOBS

The challenge introduced combining multiple wildcards in a single pattern.

## My Solve

**Flag:** `pwn.college{M5ciknmjmwPeO1gK7MoOYNBD6RU.0lM3kjNxwSNxAzNzEzW}`

In the problem statement, it was provided that cd /challenge/files and runing /challenge/run, providing a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p would yield the flag.
```
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run p
You got it! Here is your flag!
pwn.college{M5ciknmjmwPeO1gK7MoOYNBD6RU.0lM3kjNxwSNxAzNzEzW}
```

## What I learned

Learned to combine `*` wildcards to match substrings appearing anywhere in filenames.

## References

The problem statement provided was used as the reference.

# 6. MIXING GLOBS

The challenge introduced mixing bracket expressions with wildcards for refined matching.

## My Solve

**Flag:** `pwn.college{EpmdLQYpMeju54fBafkiRus_-9O.QX1IDO0wSNxAzNzEzW}`

In the problem statement, it was provided that cd /challenge/files and using the globbing writing a single, short (6 characters or less) glob that (when passed as an argument to /challenge/run) will match the files "challenging", "educational", and "pwning" would yield the flag.
```
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{EpmdLQYpMeju54fBafkiRus_-9O.QX1IDO0wSNxAzNzEzW}
```

## What I learned

Learned to mix character classes `[ ]` with `*` wildcards for precise filename matching.

## References

The problem statement provided was used as the reference.

# 7. EXCLUSIONARY GLOBBING

The challenge introduced negated character classes `[! ]` to exclude certain prefixes.

## My Solve

**Flag:** `pwn.college{MRZpEhLOsr8fxE68lIfAUfN-5tG.QX2IDO0wSNxAzNzEzW}`

In the problem statement, it was provided that going to /challenge/files and running /challenge/run with all files that don't start with p, w, or n would yield the flag.
```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{MRZpEhLOsr8fxE68lIfAUfN-5tG.QX2IDO0wSNxAzNzEzW}
```
## What I learned

Learned to exclude characters from matching using negated classes `[!pwn]`.

## References

The problem statement provided was used as the reference.

# 8. TAB COMPLETION 

The challenge introduced tab completion.

## My Solve

**Flag:** `pwn.college{wqlywP9fTFY5DICfucbPQXrT412.0FN0EzNxwSNxAzNzEzW}`

In the problem statement, it was provided that using tab completion to get `/challenge/pwncollege` and cat would yield the flag.
```
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​
pwn.college{wqlywP9fTFY5DICfucbPQXrT412.0FN0EzNxwSNxAzNzEzW}
```

## What I learned

Learned to use tab completion to reduce typing and discover filenames quickly.

## References

The problem statement provided was used as the reference.

# 9. MULTIPLE OPTIONS FOR TAB COMPLETION

The challenge introduced multiple options for tab completion.

## My Solve

**Flag:** `pwn.college{gmuyXwMaYozloRWcef7YkvASnsQ.0lN0EzNxwSNxAzNzEzW}`

In the problem statement, it was provided that tab-completing from /challenge/files/p or so to and arrive at the flag and cat flag_file would yield the flag.
```
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-
pwncollege-family pwncollege-flag pwncollege-flamingo pwncollege-flyswatter pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat pwncollege-flag
pwn.college{gmuyXwMaYozloRWcef7YkvASnsQ.0lN0EzNxwSNxAzNzEzW}
```
## What I learned

Learned that pressing tab twice lists all possible completions for a given prefix.

## References

The problem statement provided was used as the reference.

# 10. TAB COMPLETION ON COMMANDS

The challenge introduced tab completion on commands.

## My Solve

**Flag:** `pwn.college{8dNGLhGGUxxOuJ2JNJYs4Aad95q.0VN0EzNxwSNxAzNzEzW}`

In the problem statement, it was provided that command that tab completing with pwncollege would yield the flag.
```
hacker@globbing~tab-completion-on-commands:~$ pwncollege-19650
Correct! Here is your flag:
pwn.college{8dNGLhGGUxxOuJ2JNJYs4Aad95q.0VN0EzNxwSNxAzNzEzW}
```
## What I learned

Learned that tab completion can be used for commands. 

## References

The problem statement provided was used as the reference.
