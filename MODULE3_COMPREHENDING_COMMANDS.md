# MODULE3_COMPREHENDING_COMMANDS

# 1. CAT NOT THE PET BUT THE COMMAND

The challenge introduced the cat command and its basic functionality for reading file contents.

## My Solve

**Flag:** `pwn.college{QFx7uwiVw7XchP1nB1uxUEwwTwO.QXxcTN0wSNxAzNzEzW}`

The problem required using the cat command to read the contents of a file named "flag" in the current directory.
```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{QFx7uwiVw7XchP1nB1uxUEwwTwO.QXxcTN0wSNxAzNzEzW}
```

## What I learned

Learned about the cat command and how it displays the contents of files to the terminal.

## References

The problem statement provided was used as the reference.


# 2. CATTING ABSOLUTE PATHS

The challenge focused on using cat with absolute paths to read files located anywhere in the filesystem.

## My Solve

**Flag:** `pwn.college{scYVrfmJCbWhaYhVMpd1V8fvWtK.QX5ETO0wSNxAzNzEzW}`

The problem required reading the flag file using its absolute path. 
```
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{scYVrfmJCbWhaYhVMpd1V8fvWtK.QX5ETO0wSNxAzNzEzW}
```

## What I learned

Learned how to use cat with absolute paths to access files from any location in the filesystem.

## References

The problem statement was used as the reference.


# 3. MORE CATTING PRACTICE

This challenge provided more practice with the cat command using absolute paths to different directories.

## My Solve

**Flag:** `pwn.college{ILvyZ0OLHt5nBcCqJNaSrwGH4Je.QXwITO0wSNxAzNzEzW}`

The challenge required reading a flag from /usr/include/video/flag without changing directories.
```
hacker@commands~more-catting-practice:~$ cat /usr/include/video/flag
pwn.college{ILvyZ0OLHt5nBcCqJNaSrwGH4Je.QXwITO0wSNxAzNzEzW}
```

## What I learned

Learned the importance of absolute paths when accessing files in different directories without navigation.

## References

The problem statement provided was used as the reference.


# 4. GREPPING FOR A NEEDLE IN A HAYSTACK

The challenge introduced the grep command for searching specific patterns within files.

## My Solve

**Flag:** `pwn.college{kkkUfuHoiZBVhXAnpwwiQzl_CLw.QX3EDO0wSNxAzNzEzW}`

The problem required using grep to search for "pwn.college" pattern in a large data file.
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{kkkUfuHoiZBVhXAnpwwiQzl_CLw.QX3EDO0wSNxAzNzEzW}
```

## What I learned

Learned about the grep command and how it can efficiently search for specific patterns in large files.

## References

The problem statement was used as the reference.


# 5. COMPARING FILES

This challenge introduced the diff command for comparing the contents of two files.

## My Solve

**Flag:** `pwn.college{kI5AIDBh8Ij1w62sYJdblzVG7LF.01MwMDOxwSNxAzNzEzW}`

The problem required using diff to find differences between two files, where one contained decoys and the other contained both decoys and the real flag.
```
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
84a85

pwn.college{kI5AIDBh8Ij1w62sYJdblzVG7LF.01MwMDOxwSNxAzNzEzW}
```

## What I learned

Learned how to use the diff command to identify differences between files, which is useful for finding changes or additions.

## References

The problem statement provided was used as the reference.


# 6. LISTING FILES

The challenge focused on using the ls command to list directory contents and identify the correct executable file.

## My Solve

**Flag:** `pwn.college{o6y_p3UVoq0IOI6l46p9nB65k-W.QX4IDO0wSNxAzNzEzW}`

The problem required listing the challenge directory contents and executing the renamed file instead of the expected one.
```
hacker@commands~listing-files:~$ ls /challenge
24851-renamed-run-25596 DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/24851-renamed-run-25596
Yahaha, you found me! Here is your flag:
pwn.college{o6y_p3UVoq0IOI6l46p9nB65k-W.QX4IDO0wSNxAzNzEzW}
```

## What I learned

Learned the importance of using ls to verify file names before attempting to execute them, especially when files have been renamed.

## References

The problem statement was used as the reference.


# 7. TOUCHING FILES

This challenge introduced the touch command for creating empty files and directories.

## My Solve

**Flag:** `pwn.college{oG3ZFBkxbbQ2P9e0F74ROURZT9P.QXwMDO0wSNxAzNzEzW}`

The problem required creating two specific files using touch before running the challenge program.
```
hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{oG3ZFBkxbbQ2P9e0F74ROURZT9P.QXwMDO0wSNxAzNzEzW}
```

## What I learned

Learned about the touch command and how it creates empty files, which is useful for file manipulation tasks.

## References

The problem statement provided was used as the reference.


# 8. REMOVING FILES

The challenge focused on using the rm command to delete files from the filesystem.

## My Solve

**Flag:** `pwn.college{wIXHUUMoNVN69Id6ojYyLhz174g.QX2kDM1wSNxAzNzEzW}`

The problem required removing a specific file named "delete_me" before running the check program.
```
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{wIXHUUMoNVN69Id6ojYyLhz174g.QX2kDM1wSNxAzNzEzW}
```

## What I learned

Learned how to use the rm command safely to remove files when required by system tasks.

## References

The problem statement was used as the reference.


# 9. MOVING FILES

This challenge introduced the mv command for moving and renaming files within the filesystem.

## My Solve

**Flag:** `pwn.college{YhRj-gi8d5kOQf1ZC_utEqHjijw.0VOxEzNxwSNxAzNzEzW}`

The problem required moving the flag file to a specific location with a specific name.
```
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{YhRj-gi8d5kOQf1ZC_utEqHjijw.0VOxEzNxwSNxAzNzEzW}
```

## What I learned

Learned about the mv command and how it can both move files to different locations and rename them simultaneously.

## References

The problem statement provided was used as the reference.


# 10. HIDDEN FILES

The challenge focused on finding and accessing hidden files that start with a dot (.) character.

## My Solve

**Flag:** `pwn.college{YU4jc7Kcx5j-H7eYXmKH0IX8rSW.QXwUDO0wSNxAzNzEzW}`

The problem required using ls -a to show hidden files and then accessing the hidden flag file.
```
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
. .dockerenv bin challenge etc lib lib64 media nix proc run srv tmp var
.. .flag-38411547519433 boot dev home lib32 libx32 mnt opt root sbin sys usr
hacker@commands~hidden-files:/$ cat .flag-38411547519433
pwn.college{YU4jc7Kcx5j-H7eYXmKH0IX8rSW.QXwUDO0wSNxAzNzEzW}
```

## What I learned

Learned about hidden files in Linux and how to use ls -a to display files that start with a dot character.

## References

The problem statement was used as the reference.


# 11. MAKING DIRECTORIES

This challenge introduced the mkdir command for creating new directories in the filesystem.

## My Solve

**Flag:** `pwn.college{cTNz5vY3Y4raAYumWoQcXKpr6SU.QXxMDO0wSNxAzNzEzW}`

The problem required creating a directory, navigating to it, creating a file within it, and then running the challenge program.
```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{cTNz5vY3Y4raAYumWoQcXKpr6SU.QXxMDO0wSNxAzNzEzW}
```

## What I learned

Learned how to use mkdir to create directories and the importance of directory structure in organizing files.

## References

The problem statement provided was used as the reference.


# 12. FINDING FILES

The challenge focused on using the find command to locate files based on their names across the filesystem.

## My Solve

**Flag:** `pwn.college{ovy7PHDOMp3U7aw77ZFMobifJNH.QXyMDO0wSNxAzNzEzW}`

The problem required using find to search for files named "flag", then accessing the correct one.
```
hacker@commands~finding-files:~$ cd /
hacker@commands~finding-files:/$ find -name flag
./opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/irq/dce80/flag
hacker@commands~finding-files:/$ cat ./opt/linux/linux-5.4/drivers/gpu/drm/amd/display/dc/irq/dce80/flag
pwn.college{ovy7PHDOMp3U7aw77ZFMobifJNH.QXyMDO0wSNxAzNzEzW}
```

## What I learned

Learned about the find command and how it can efficiently search for files by name across the entire filesystem, despite permission errors in some directories.

## References

The problem statement was used as the reference.


# 13. LINKING FILES

This challenge introduced symbolic links and the ln command for creating links between files.

## My Solve

**Flag:** `pwn.college{kU9gLyApHyEQ0iA3vgRZAQqAeuX.QX5ETN1wSNxAzNzEzW}`

The problem required creating a symbolic link to the flag file and then having the challenge program read it.
```
hacker@commands~linking-files:~$ ln -s /flag ~/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{kU9gLyApHyEQ0iA3vgRZAQqAeuX.QX5ETN1wSNxAzNzEzW}
```

## What I learned

Learned about symbolic links and how the ln -s command creates links that point to other files, allowing access through different paths.

## References

The problem statement provided was used as the reference.

