# MODULE11_PERCEIVING_PERMISSIONS

# 1. CHANGING FILE OWNERSHIP

The challenge introduced using `chown` to change a file’s owner.

## My Solve

**Flag:** `pwn.college{sHRPVxx-KZ8STER4seqn95qCLSw.QXxEjN0wSNxAzNzEzW}`

In the problem statement, it was provided that the hacker user can `chown hacker /flag` and then read it.
``` 
hacker@permissions~changing-file-ownership:$ chown hacker /flag
hacker@permissions~changing-file-ownership:$ cat /flag
pwn.college{sHRPVxx-KZ8STER4seqn95qCLSw.QXxEjN0wSNxAzNzEzW}
hacker@permissions~changing-file-ownership:~$
``` 

## What I learned

Learned to change file ownership with `chown` to gain read access.

## References

The problem statement provided was used as the reference.

# 2. CHANGING GROUP OWNERSHIP

The challenge introduced using `chgrp` to change a file’s group.

## My Solve

**Flag:** `pwn.college{8J1EktN2Tr-qYbRUt75cTUN9As-.QXxcjM1wSNxAzNzEzW}`

In the problem statement, it was provided that the hacker user can `chgrp hacker /flag` and then read it.
``` 
hacker@permissions~groups-and-files:$ chgrp hacker /flag
hacker@permissions~groups-and-files:$ cat /flag
pwn.college{8J1EktN2Tr-qYbRUt75cTUN9As-.QXxcjM1wSNxAzNzEzW}
hacker@permissions~groups-and-files:~$
``` 

## What I learned

Learned to change file group ownership with `chgrp` to gain read access.

## References

The problem statement provided was used as the reference.

# 3. DETERMINING AND CHANGING A RANDOM GROUP

The challenge introduced using `id` to discover the user’s group and then `chgrp`.

## My Solve

**Flag:** `pwn.college{cG8ZLaxMz-bk2_kqwVGD8iKDsc9.QXycjM1wSNxAzNzEzW}`

In the problem statement, it was provided that the hacker user’s group is randomized; use `id` to find it and then `chgrp`.
``` 
hacker@permissions~fun-with-groups-names:$ id
uid=1000(hacker) gid=1000(grp2276) groups=1000(grp2276)
hacker@permissions~fun-with-groups-names:$ chgrp grp2276 /flag
hacker@permissions~fun-with-groups-names:$ cat /flag
pwn.college{cG8ZLaxMz-bk2_kqwVGD8iKDsc9.QXycjM1wSNxAzNzEzW}
hacker@permissions~fun-with-groups-names:~$
``` 

## What I learned

Learned to identify the user’s primary group with `id` and change the file’s group.

## References

The problem statement provided was used as the reference.

# 4. CHANGING FILE PERMISSIONS

The challenge introduced using `chmod` to grant read permission.

## My Solve

**Flag:** `pwn.college{YRKwbr80__w_xw_EwDf7R1vfsx8.QXzcjM1wSNxAzNzEzW}`

In the problem statement, it was provided that you can `chmod a+r /flag` as hacker to make it readable.
``` 
hacker@permissions~changing-permissions:$ chmod a+r /flag
hacker@permissions~changing-permissions:$ cat /flag
pwn.college{YRKwbr80__w_xw_EwDf7R1vfsx8.QXzcjM1wSNxAzNzEzW}
hacker@permissions~changing-permissions:~$
``` 

## What I learned

Learned to grant read permission to all with `chmod a+r`.

## References

The problem statement provided was used as the reference.

# 5. MAKING A PROGRAM EXECUTABLE

The challenge introduced using `chmod` to set the execute bit.

## My Solve

**Flag:** `pwn.college{wiUnz22PKuQd7VylSgL3pqconPx.QXyEjN0wSNxAzNzEzW}`

In the problem statement, it was provided that `/challenge/run` must be made executable with `chmod a+x`.
``` 
hacker@permissions~executable-files:$ chmod a+x /challenge/run
hacker@permissions~executable-files:$ /challenge/run
Successful execution! Here is your flag:
pwn.college{wiUnz22PKuQd7VylSgL3pqconPx.QXyEjN0wSNxAzNzEzW}
hacker@permissions~executable-files:~$
``` 

## What I learned

Learned to grant execute permission with `chmod a+x`.

## References

The problem statement provided was used as the reference.

# 6. PERMISSION-TWEAKING PRACTICE

The challenge introduced iterative use of `chmod` to match displayed permission requirements across eight rounds.

## My Solve

**Flag:** `pwn.college{IYhZI4ebfrZOiazLFzNSTl1jYaz.QXwEjN0wSNxAzNzEzW}`

In the problem statement, it was provided that correctly applying the required `chmod` changes eight times in a row unlocks the ability to `chmod u+r /flag`.
``` 
hacker@permissions~permission-tweaking-practice:$ /challenge/run
… (8 rounds of chmod challenges) …
hacker@permissions~permission-tweaking-practice:$ chmod u+r /flag
hacker@permissions~permission-tweaking-practice:$ cat /flag
pwn.college{IYhZI4ebfrZOiazLFzNSTl1jYaz.QXwEjN0wSNxAzNzEzW}
hacker@permissions~permission-tweaking-practice:~$
``` 

## What I learned

Learned to read detailed permission requirements and apply complex `chmod` operations iteratively.

## References

The problem statement provided was used as the reference.

# 7. PERMISSIONS SETTING PRACTICE WITH `=` AND `-`

The challenge introduced using symbolic modes (with `=` and `-`) in `chmod` to set exact permission sets.

## My Solve

**Flag:** `pwn.college{kwP-4bYinArC2laE4WBOclLl_kr.QXzETO0wSNxAzNzEzW}`

In the problem statement, it was provided that chaining `=` and `-` in `chmod` over eight rounds unlocks read access to `/flag`.
``` 
hacker@permissions~permissions-setting-practice:$ /challenge/run
… (8 rounds using chmod u=x,g=x,o=rwx, etc.) …
hacker@permissions~permissions-setting-practice:$ chmod u=r /flag
hacker@permissions~permissions-setting-practice:$ cat /flag
pwn.college{kwP-4bYinArC2laE4WBOclLl_kr.QXzETO0wSNxAzNzEzW}
hacker@permissions~permissions-setting-practice:~$
``` 

## What I learned

Learned to use `chmod u=…,g=…,o=…` and `-` to set precise permission bits.

## References

The problem statement provided was used as the reference.

# 8. SETTING THE SUID BIT

The challenge introduced using `chmod u+s` to add the SUID bit to an executable.

## My Solve

**Flag:** `pwn.college{sXRyrIEBKEIkoLGAc7PFdjaC5XS.QXzEjN0wSNxAzNzEzW}`

In the problem statement, it was provided that setting the SUID bit on `/challenge/getroot` allows spawning a root shell to read `/flag`.
``` 
hacker@permissions~the-suid-bit:$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell…
root@permissions~the-suid-bit:# cat /flag
pwn.college{sXRyrIEBKEIkoLGAc7PFdjaC5XS.QXzEjN0wSNxAzNzEzW}
root@permissions~the-suid-bit:#
``` 
## What I learned

Learned to add the SUID bit with `chmod u+s` to execute a program as its owner.

## References

The problem statement provided was used as the reference.
