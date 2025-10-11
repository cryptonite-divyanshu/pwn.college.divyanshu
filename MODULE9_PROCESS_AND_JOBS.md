# MODULE9_PROCESS_AND_JOBS

# 1. LISTING PROCESSES

The challenge introduced using `ps aux` (or `ps -ef`) to list running processes and locate a hidden challenge binary.

## My Solve

**Flag:** `pwn.college{MAQIQvMcwfxQAll2ILHNidCPwvo.QX4MDO0wSNxAzNzEzW}`

In the problem statement, it was provided that the renamed `/challenge/run` binary appears in the process list and must be executed directly.
```
hacker@processes~listing-processes:~$ ps aux | grep challenge
root 132 0.0 0.0 4132 2560 ? S 17:38 0:00 /challenge/12782-run-12533
hacker 153 0.0 0.0 230696 2560 pts/0 S+ 17:38 0:00 grep --color=auto challenge
hacker@processes~listing-processes:~$ /challenge/12782-run-12533
Yahaha, you found me! Here is your flag:
pwn.college{MAQIQvMcwfxQAll2ILHNidCPwvo.QX4MDO0wSNxAzNzEzW}
hacker@processes~listing-processes:~$
```
## What I learned

Learned to locate and execute a hidden binary by inspecting the process list.

## References

The problem statement provided was used as the reference.

# 2. KILLING PROCESSES

The challenge introduced using `kill` to terminate a blocking process.

## My Solve

**Flag:** `pwn.college{wwuMjThdt4r1bV7tQaTnz_9oHc4.QXyQDO0wSNxAzNzEzW}`

In the problem statement, it was provided that `/challenge/dont_run` must be killed before `/challenge/run` will execute.
```
hacker@processes~killing-processes:~$ ps aux | grep dont_run
hacker 136 0.0 0.0 231576 3520 ? Ss 17:43 0:00 /challenge/dont_run
hacker 155 0.0 0.0 230696 2560 pts/0 S+ 17:43 0:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{wwuMjThdt4r1bV7tQaTnz_9oHc4.QXyQDO0wSNxAzNzEzW}
hacker@processes~killing-processes:~$
```
## What I learned

Learned to terminate a specific process by PID to unblock another process.

## References

The problem statement provided was used as the reference.

# 3. INTERRUPTING PROCESSES

The challenge introduced using **Ctrl-C** to send SIGINT and interrupt a running process.

## My Solve

**Flag:** `pwn.college{UzBf7TiqA6IT_0_9Jo0G-HHBq8O.QXzQDO0wSNxAzNzEzW}`

In the problem statement, it was provided that `/challenge/run` must be interrupted with Ctrl-C to yield the flag.
```
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{UzBf7TiqA6IT_0_9Jo0G-HHBq8O.QXzQDO0wSNxAzNzEzW}
hacker@processes~interrupting-processes:~$
```
## What I learned

Learned to interrupt a foreground process using Ctrl-C (SIGINT).

## References

The problem statement provided was used as the reference.

# 4. KILLING A FIFO-HOGGING PROCESS

The challenge introduced identifying and killing a process writing to a named pipe (FIFO).

## My Solve

**Flag:** `pwn.college{QjpQ4zKjbiuN869vPOh4btAO2Po.0FNzMDOxwSNxAzNzEzW}`

In the problem statement, it was provided that `/challenge/decoy` must be killed so `/challenge/run` can write the real flag to `/tmp/flag_fifo`.
```
TERMINAL1:
hacker@processes~killing-misbehaving-processes:~$ ps -ef
UID PID PPID C STIME TTY TIME CMD
...
hacker 142 139 0 12:04 ? 00:00:00 /usr/bin/python /challenge/decoy
...
hacker@processes~killing-misbehaving-processes:~$ kill 142

TERMINAL2:
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{PLXi-oyBFB.ucXN369lsOGrk0I35bvuO7wLb7Zeor6d4wf5}
... (decoys)
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!

TERMINAL2:
pwn.college{QjpQ4zKjbiuN869vPOh4btAO2Po.0FNzMDOxwSNxAzNzEzW}
```

## What I learned

Learned to identify and kill a process hogging a FIFO to allow the intended writer to succeed.

## References

The problem statement provided was used as the reference.

# 5. SUSPENDING PROCESSES

The challenge introduced using Ctrl-Z to suspend a foreground process.

## My Solve

**Flag:** `pwn.college{YiJOG1oLuxwSMsqK2cnUOU1XXy1.QX1QDO0wSNxAzNzEzW}`

In the problem statement, it was provided that suspending `/challenge/run` and then launching it again counts as two copies.
```
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!
... (no second process)
^Z

Stopped /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
... (two copies detected)
Yay, I found another version of me! Here is the flag:
pwn.college{YiJOG1oLuxwSMsqK2cnUOU1XXy1.QX1QDO0wSNxAzNzEzW}
hacker@processes~suspending-processes:~$
```

## What I learned

Learned to suspend a process to the background with Ctrl-Z and verify with process listing.

## References

The problem statement provided was used as the reference.

# 6. RESUMING PROCESSES

The challenge introduced using `fg` to resume a suspended process in the foreground.

## My Solve

**Flag:** `pwn.college{o0sMZfAl43LUFDBuKkY66aMOHJE.QX2QDO0wSNxAzNzEzW}`

In the problem statement, it was provided that suspending and then resuming `/challenge/run` with `fg` yields the flag.
```
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z

Stopped /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{o0sMZfAl43LUFDBuKkY66aMOHJE.QX2QDO0wSNxAzNzEzW}
Don't forget to press Enter to quit me!
hacker@processes~resuming-processes:~$
```
## What I learned

Learned to resume a suspended process in the foreground using `fg`.

## References

The problem statement provided was used as the reference.

# 7. BACKGROUNDING PROCESSES

The challenge introduced using `bg` to resume a suspended process in the background.

## My Solve

**Flag:** `pwn.college{I3iLQR_Vir0a_2cWOjHDMkfIjmt.QX3QDO0wSNxAzNzEzW}`

In the problem statement, it was provided that suspending `/challenge/run`, using `bg`, then launching a new copy yields the flag.
```
hacker@processes~backgrounding-processes:~$ /challenge/run
...
^Z

Stopped /challenge/run
hacker@processes~backgrounding-processes:~$ bg

/challenge/run &
hacker@processes~backgrounding-processes:~$ /challenge/run
... (background + foreground)
Yay, I found another version of me running in the background! Here is the flag:
pwn.college{I3iLQR_Vir0a_2cWOjHDMkfIjmt.QX3QDO0wSNxAzNzEzW}
hacker@processes~backgrounding-processes:~$
```

## What I learned

Learned to resume a suspended process in the background using `bg` and verify with process listing.

## References

The problem statement provided was used as the reference.

# 8. FOREGROUNDING PROCESSES

The challenge introduced re-foregrounding a backgrounded process with `fg`.

## My Solve

**Flag:** `pwn.college{4M2I53iUKf4urSMJD5QIfmqty0Y.QX4QDO0wSNxAzNzEzW}`

In the problem statement, it was provided that suspending, backgrounding, then foregrounding `/challenge/run` yields the flag.
```
hacker@processes~foregrounding-processes:~$ /challenge/run
...
^Z

Stopped /challenge/run
hacker@processes~foregrounding-processes:~$ bg

/challenge/run &
hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{4M2I53iUKf4urSMJD5QIfmqty0Y.QX4QDO0wSNxAzNzEzW}
hacker@processes~foregrounding-processes:~$
```
## What I learned

Learned to bring a backgrounded process back to the foreground using `fg`.

## References

The problem statement provided was used as the reference.

# 9. STARTING BACKGROUNDED PROCESSES

The challenge introduced appending `&` to start a process in the background immediately.

## My Solve

**Flag:** `pwn.college{4YKjc1pvQMZX5Ab0FuPkXP481II.QX5QDO0wSNxAzNzEzW}`

In the problem statement, it was provided that launching `/challenge/run &` starts it in the background and yields the flag.
```
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
140
hacker@processes~starting-backgrounded-processes:~$
Anyways! Here is your flag!
pwn.college{4YKjc1pvQMZX5Ab0FuPkXP481II.QX5QDO0wSNxAzNzEzW}

Done /challenge/run
```
## What I learned

Learned to start a process in the background by appending `&` to the command.

## References

The problem statement provided was used as the reference.

# 10. PROCESS EXIT CODES

The challenge introduced retrieving a process’s exit code with `$?` and submitting it.

## My Solve

**Flag:** `pwn.college{swrjGDCyjHFbeKoZ7Sue5Ti9Ve_.QX5YDO1wSNxAzNzEzW}`

In the problem statement, it was provided that `/challenge/get-code` exits non-zero and `$?` must be passed to `/challenge/submit-code`.
```
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
33
hacker@processes~process-exit-codes:~$ /challenge/submit-code 33
CORRECT! Here is your flag:
pwn.college{swrjGDCyjHFbeKoZ7Sue5Ti9Ve_.QX5YDO1wSNxAzNzEzW}
hacker@processes~process-exit-codes:~$
```
## What I learned

Learned to capture a command’s exit status with `$?` and use it as an argument for submission.

## References

The problem statement provided was used as the reference.
