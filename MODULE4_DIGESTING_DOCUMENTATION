# MODULE4_DIGESTING_DOCUMENTATION

# 1. LEARNING FROM DOCUMENTATION

The challenge introduced how to use program documentation to determine the correct arguments for execution.

## My Solve

**Flag:** `pwn.college{UTuVu_a2ngRNB6YBD5zkGVtnTZc.QX0ITO0wSNxAzNzEzW}`

In the problem statement, it was provided that invoking the challenge program with the correct argument would provide the flag.
```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{UTuVu_a2ngRNB6YBD5zkGVtnTZc.QX0ITO0wSNxAzNzEzW}
```
## What I learned

Learned about using program documentation to determine valid command-line arguments.

## References

The problem statement provided was used as the reference.

# 2. LEARNING COMPLEX USAGE

The challenge focused on using programs with additional arguments to perform specific file operations.

## My Solve

**Flag:** `pwn.college{cLe4A6hmQd_y4z5Yj7zLlqAzX11.QX1ITO0wSNxAzNzEzW}`

I was provided in the problem statement that the challenge program could print files when given the correct argument format.
```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{cLe4A6hmQd_y4z5Yj7zLlqAzX11.QX1ITO0wSNxAzNzEzW}
```

## What I learned

Learned how to pass file paths as arguments to programs for complex operations.

## References

The problem statement provided was used as the reference.

# 3. READING MANUALS

The challenge introduced the man command for reading manual pages to understand program functionality.

## My Solve

**Flag:** `pwn.college{Qil0E16Ax1ijDiuYgh-60Jc-Ipb.QX0EDO0wSNxAzNzEzW}`

Reading the manual page and finding the correct argument yielded the flag.
```
hacker@man~reading-manuals:~$ man challenge
CHALLENGE(1) Challenge Commands CHALLENGE(1)

NAME
/challenge/challenge - print the flag!

SYNOPSIS
challenge OPTION

DESCRIPTION
Output the flag when called with the right arguments.

   --fortune
           read a fortune

   --version
           output version information and exit

   --ilxiji NUM
           print the flag if NUM is 016
AUTHOR
Written by Zardus.

REPORTING BUGS
The repository for this dojo: https://github.com/pwncollege/linux-luminarium/

SEE ALSO
man(1) bash-builtins(7)

Manual page challenge(1) line 1/31 87% (press h for help or q to quit)
hacker@man~reading-manuals:~$ /challenge/challenge --ilxiji 016
Correct usage! Your flag: pwn.college{Qil0E16Ax1ijDiuYgh-60Jc-Ipb.QX0EDO0wSNxAzNzEzW}
```

## What I learned

Learned how to use man pages to discover program options and their required arguments.

## References

The man page for the challenge program was used as the reference.

# 4. SEARCHING MANUALS

The challenge required searching through manual pages to find hidden or undocumented options.

## My Solve

**Flag:** `pwn.college{Y5j-XyfNoYHrVooWieR2ng1uqlc.QX1EDO0wSNxAzNzEzW}`

Exploring the manual and discovering hidden options yielded the flag.
```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --svxuepb
Initializing...
Correct usage! Your flag: pwn.college{Y5j-XyfNoYHrVooWieR2ng1uqlc.QX1EDO0wSNxAzNzEzW}
```

## What I learned

Learned that programs sometimes accept undocumented or hidden options that require exploration.

## References

The problem statement and manual exploration was used as the reference.

# 5. SEARCHING FOR MANUALS

The challenge introduced using man -k to search for related programs and their documentation.

## My Solve

**Flag:** `pwn.college{w1ZjRjdwTMc4GIc8qcS3TBmIpW_.QX2EDO0wSNxAzNzEzW}`

Using man -k to discover related programs and reading their documentation yielded the flag.
```
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k challenge
wjjdwccqcm (1) - print the flag!
hacker@man~searching-for-manuals:~$ man wjjdwccqcm

CHALLENGE(1) Challenge Commands CHALLENGE(1)

NAME
/challenge/challenge - print the flag!

SYNOPSIS
challenge OPTION

DESCRIPTION
Output the flag when called with the right arguments.

   --fortune
           read a fortune

   --version
           output version information and exit

   --wjjdwc NUM
           print the flag if NUM is 148
AUTHOR
Written by Zardus.

REPORTING BUGS
The repository for this dojo: https://github.com/pwncollege/linux-luminarium/

SEE ALSO
man(1) bash-builtins(7)

pwn.college May 2024 CHALLENGE(1)
Manual page wjjdwccqcm(1) line 1/31 (END) (press h for help or q to quit)
hacker@man~searching-for-manuals:~$ /challenge/challenge --wjjdwc 148
Correct usage! Your flag: pwn.college{w1ZjRjdwTMc4GIc8qcS3TBmIpW_.QX2EDO0wSNxAzNzEzW}
```
## What I learned

Learned how to use man -k to search for programs by keyword and discover related documentation.

## References

The man pages and search results were used as the reference.

# 6. HELPFUL PROGRAMS

The challenge focused on using program help options to discover required values and arguments.

## My Solve

**Flag:** `pwn.college{o76_xN75g4WRMq_0bzxhypt7nEd.QX3IDO0wSNxAzNzEzW}`

Using the program's help functionality to discover the required secret value yielded the flag.
```
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
-h, --help show this help message and exit
--fortune read your fortune
-v, --version get the version number
-g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
get the flag, if given the correct value
-p, --print-value print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 767
hacker@man~helpful-programs:~$ /challenge/challenge -g 767
Correct usage! Your flag: pwn.college{o76_xN75g4WRMq_0bzxhypt7nEd.QX3IDO0wSNxAzNzEzW}
```

## What I learned

Learned that many programs provide helpful information through --help or -h flags that reveal secret values or usage patterns.

## References

The program's help output was used as the reference.

# 7. HELP FOR BUILTINS

The challenge introduced using the help command for bash builtin functions to understand their usage.

## My Solve

**Flag:** `pwn.college{wbxAL9OVEVf3nt0Bw54z7LF-zm4.QX0ETO0wSNxAzNzEzW}`

Using the help command to discover the required secret argument yielded the flag.
```
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
This builtin command will read you the flag, given the right arguments!

Options:
  --fortune         display a fortune
  --version         display the version
  --secret VALUE    prints the flag, if VALUE is correct

You must be sure to provide the right value to --secret. That value is "wbxAL9OV".
hacker@man~help-for-builtins:~$ challenge --secret wbxAL9OV
Correct! Here is your flag!
pwn.college{wbxAL9OVEVf3nt0Bw54z7LF-zm4.QX0ETO0wSNxAzNzEzW}
```

## What I learned

Learned that bash builtin commands use the help command instead of man pages, and they can provide secret values directly in their help text.

## References

The help command output was used as the reference.
