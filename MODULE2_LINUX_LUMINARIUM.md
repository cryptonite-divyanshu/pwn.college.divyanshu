# MODULE2_LINUX_LUMINARIUM
# 1. THE ROOT
The pwn command was introduced via its absolute path.

## My Solve
**Flag:** `pwn.college{s0K_pKLCQDISbuagtR7PmcuHupw.QX4cTO0wSNxAzNzEzW}`

In the problem statement, it was provided that, invoking pwn via absolute path would provide the flag
```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{s0K_pKLCQDISbuagtR7PmcuHupw.QX4cTO0wSNxAzNzEzW}
```

## What I learned
Learned about the root directory and how to invoke a program via its absolute path.

## References
The problem statement was the reference used.


# 2. Program and absolute paths
The challenge introduced the challenge directory and the goal was to run the 'run' program via its absolute path.

## My solve
**Flag:** `pwn.college{IF9FDnik4KyzDOSETX3B5NgkJFX.QX1QTN0wSNxAzNzEzW}`

I was provided in the problem statement that invoking the run program via its absolute path including the challenge directory would get the flag.

```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{IF9FDnik4KyzDOSETX3B5NgkJFX.QX1QTN0wSNxAzNzEzW}
```

## What I learned
Learned about the challenge directory. learned a bit deeper about programs and absolute paths.

## References
The problem statement provided was used as the reference.


# 3. Position thy self
cd command was introduced. The funcionality of '~' was expanded upon. 

## My Solve

Changing directory and invoking program yielded the flag.

**Flag:** `pwn.college{sp33803dnYFPjIXtDcsYacssjc1.QX2QTN0wSNxAzNzEzW}`

```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the cd utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /
hacker@paths~position-thy-self:/$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{sp33803dnYFPjIXtDcsYacssjc1.QX2QTN0wSNxAzNzEzW}
```

First invoked the run program via /challenge/run. 
This caused the hint to appear. 
Changed directories accordingly and invoked program to get the flag.

## What I learned
Learned how to use cd command.

## References
The problem statement was used as the reference


# 4. Position Elsewhere
The challenge required moving to the `/etc` directory before invoking the program.

## My Solve
**Flag:** `pwn.college{0y6ob-fwthS3tTag9Zz0cfIqt8x.QX3QTN0wSNxAzNzEzW}`

Moving to the required directory and invoking the program yielded the flag.

```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /etc directory.
Please use the cd utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /etc
hacker@paths~position-elsewhere:/etc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0y6ob-fwthS3tTag9Zz0cfIqt8x.QX3QTN0wSNxAzNzEzW}
```

## What I learned
Better understood 'cd' command and how to invoke programs.

## References
The problem statement provided was used as the reference.


# 5. Position Yet Elsewhere
The challenge required navigating to a deeper directory `/usr/share/build-essential`.

## My Solve
**Flag:** `pwn.college{sHk6nOYkP7hpTnNPWtEqzhnp1t6.QX4QTN0wSNxAzNzEzW}`

Moving to the required directory and invoking the program yielded the flag.

```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/build-essential directory.
Please use the cd utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /usr/share/build-essential directory
bash: cd: too many arguments
hacker@paths~position-yet-elsewhere:~$ cd /usr/share/build-essential
hacker@paths~position-yet-elsewhere:/usr/share/build-essential$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{sHk6nOYkP7hpTnNPWtEqzhnp1t6.QX4QTN0wSNxAzNzEzW}
```

## What I learned
Learned to go into deeper directories via the 'cd' command.

## References
The problem statement provided was used as the reference.


# 6. Implicit Relative Paths
The challenge required using a relative path instead of an absolute one.

## My Solve
**Flag:** `pwn.college{sL78ezWOoBeZWDgAE-W6QuDZQca.QX5QTN0wSNxAzNzEzW}`

Moving to the required directory and invoking the program via its relative path yielded the flag.

```
hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the cd utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{sL78ezWOoBeZWDgAE-W6QuDZQca.QX5QTN0wSNxAzNzEzW}
```

## What I learned
Learned how changing directories can be useful for invoking programs with their relative paths.

## References
The problem statement provided was used as the reference.


# 7. Explicit Relative Paths
The challenge focused on explicitly using `./` to run a program from the current directory.

## My Solve
**Flag:** `pwn.college{M8AeCaKjDFp4LR4hxSszlMOh9hP.QXwUTN0wSNxAzNzEzW}`

Moving to the required directory and invoking the program using './' yielded the flag.

```
hacker@paths~explicit-relative-paths-from-:~$ ./challenge
bash: ./challenge: No such file or directory
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge
bash: ./challenge: Is a directory
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{M8AeCaKjDFp4LR4hxSszlMOh9hP.QXwUTN0wSNxAzNzEzW}
```

## What I learned
Learned the use of `./` and other similar ways to shorten the paths and invoke programs via explicit relative paths. 
Got to know I was using 'naked' paths till now :o

## References
The problem statement provided was used as the reference.


# 8. Implicit Relative Path
The challenge required entering the `/challenge` directory and running the program with `./`.

## My Solve
**Flag:** `pwn.college{0M0kCIS6fIgOZXsxwbvK0zgehll.QXxUTN0wSNxAzNzEzW}`

Moving to the required directory and invoking the program using './' yielded the flag.

```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{0M0kCIS6fIgOZXsxwbvK0zgehll.QXxUTN0wSNxAzNzEzW}
```

## What I learned
Learned how to change into a directory and run its program using `./`.
Learned the reason why Linux does'nt run these 'naked' paths automatically as doing so can cause it to execute other stuff there which have same names as well as core system functionalities.

## References
The problem statement provided was used as the reference.


# 9. Home Sweet Home
The challenge introduced arguments and tilde `~` expansion. A file path under the home directory needed to be passed to `/challenge/run`.

## My Solve
**Flag:** `pwn.college{wew_a1iZ2pJuXXW3iSu1_zNdYGs.QXzMDO0wSNxAzNzEzW}`

First tried creating a file t using 'touch' command and writing the flag into it.

It failed as there was a previous instance of t.txt being created which had a larger name than the one specified in the challenge.

Tried creating t in home but permission was denied.

Tried creating others but they failed as well due to prvious instances where a directory with similar name was created.

Finally tried creating file m.

Created successfully.

Wrote the copy of the flag onto m and received it.

```
hacker@paths~home-sweet-home:~$ /challenge/run
You must provide an argument to /challenge/run when you invoke it!
hacker@paths~home-sweet-home:~$ touch t
hacker@paths~home-sweet-home:~$ /challenge/run ~/t
Writing the file to /home/hacker/t!
/challenge/run: line 29: /home/hacker/t: Is a directory
... and reading it back to you:
cat: /home/hacker/t: Is a directory
hacker@paths~home-sweet-home:~$ touch b
touch: cannot touch 'b': Permission denied
hacker@paths~home-sweet-home:~$ touch c
touch: cannot touch 'c': Permission denied
hacker@paths~home-sweet-home:~$ touch m
hacker@paths~home-sweet-home:~$ /challenge/run ~/m
Writing the file to /home/hacker/m!
... and reading it back to you:
pwn.college{wew_a1iZ2pJuXXW3iSu1_zNdYGs.QXzMDO0wSNxAzNzEzW}
```

## What I learned
Learned that '~' can be used to shorten paths and how it itself is shorthand for /home/hacker.

learned use of 'touch' command.

Got to know that we can't create files into home directory.

In linux by default there is no need for file extensions while using touch to create files.

Learned how to write into a file.

## References
The problem statement provided was used as the reference.

Also took the help of mentor to cross verify and validate facts when stuck.


