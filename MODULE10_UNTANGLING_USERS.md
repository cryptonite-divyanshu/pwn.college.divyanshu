# MODULE10_UNTANGLING_USERS

# 1. BECOMING ROOT WITH su

The challenge introduced using `su` with the root password to elevate privileges.

## My Solve

**Flag:** `pwn.college{UaYBEy_HquJ3cZk-KbXNOqKlk9B.QX1UDN1wSNxAzNzEzW}`

In the problem statement, it was provided that the root password is `hack-the-planet` and must be entered to become root and read `/flag`.
``` 
hacker@users~becoming-root-with-su:$ whoami
hacker
hacker@users~becoming-root-with-su:$ su
Password:
hack-the-planet
root@users~becoming-root-with-su:/home/hacker# whoami
root
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{UaYBEy_HquJ3cZk-KbXNOqKlk9B.QX1UDN1wSNxAzNzEzW}
root@users~becoming-root-with-su:#
``` 

## What I learned

Learned to use `su` with a known root password to start a root shell.

## References

The problem statement provided was used as the reference.

# 2. SWITCHING USERS WITH su

The challenge introduced using `su` with a username argument to switch to another user.

## My Solve

**Flag:** `pwn.college{ggMUP6HBv36i6adoeVnsp5VCByU.QX2UDN1wSNxAzNzEzW}`

In the problem statement, it was provided that `zardus`’ password is `dont-hack-me`, and switching to `zardus` allows execution of `/challenge/run`.
``` 
hacker@users~other-users-with-su:$ whoami
hacker
hacker@users~other-users-with-su:$ su zardus
Password:
dont-hack-me
zardus@users~other-users-with-su:/home/hacker$ whoami
zardus
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{ggMUP6HBv36i6adoeVnsp5VCByU.QX2UDN1wSNxAzNzEzW}
zardus@users~other-users-with-su:/home/hacker$
``` 

## What I learned

Learned to switch to another user by passing the username to `su`.

## References

The problem statement provided was used as the reference.

# 3. CRACKING A PASSWORD HASH WITH John

The challenge introduced using John the Ripper to crack a leaked `/etc/shadow` entry and then using `su`.

## My Solve

**Flag:** `pwn.college{4wfrzqxvRpG6x7-OmlhDziaAhfY.QX3UDN1wSNxAzNzEzW}`

In the problem statement, it was provided that `/challenge/shadow-leak` contains Zardus’s hash, which cracks to `aardvark`, then `su zardus` and run `/challenge/run`.
``` 
hacker@users~cracking-passwords:$ john /challenge/shadow-leak
Loaded 1 password hash (crypt…)
Press any key for status
aardvark (zardus)
Session completed
hacker@users~cracking-passwords:$ su zardus
Password:
aardvark
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{4wfrzqxvRpG6x7-OmlhDziaAhfY.QX3UDN1wSNxAzNzEzW}
zardus@users~cracking-passwords:/home/hacker$

``` 
## What I learned

Learned to crack a password hash with John and use the recovered password to `su`.

## References

The problem statement provided was used as the reference.

# 4. READING FILES WITH sudo

The challenge introduced using `sudo` to run commands as root without a password.

## My Solve

**Flag:** `pwn.college{wLlmnb2tyaKB0Bel6LFiC-1fX64.QX4UDN1wSNxAzNzEzW}`

In the problem statement, it was provided that the user has sudo privileges and can run `sudo cat /flag`.
``` 
hacker@users~using-sudo:$ sudo cat /flag
pwn.college{wLlmnb2tyaKB0Bel6LFiC-1fX64.QX4UDN1wSNxAzNzEzW}
hacker@users~using-sudo:$
``` 

## What I learned

Learned to use `sudo` to read protected files as root without knowing the root password.

## References

The problem statement provided was used as the reference.

