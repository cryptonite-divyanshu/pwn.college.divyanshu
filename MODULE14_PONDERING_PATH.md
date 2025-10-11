# MODULE14_PONDERING_PATH

# 1. THE PATH VARIABLE
The challenge introduced blanking out `PATH` so builtins can’t find external commands.

## My Solve

**Flag:** `pwn.college{AiQOpIIAPcGPpuBOMJqNackTZFT.QX2cDM1wSNxAzNzEzW}`

In the problem statement, it was provided that `/challenge/run` deletes `/flag` with `rm`, so clearing `PATH` prevents `rm` from being found.
```
hacker@path~the-path-variable:$ PATH=""
hacker@path~the-path-variable:$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{AiQOpIIAPcGPpuBOMJqNackTZFT.QX2cDM1wSNxAzNzEzW}
hacker@path~the-path-variable:~$
```

## What I learned

Learned that clearing `PATH` causes external commands to become unavailable in child processes.

## References

The problem statement provided was used as the reference.

# 2. SETTING PATH

The challenge introduced overwriting `PATH` to include only a directory with the needed command.

## My Solve

**Flag:** `pwn.college{QjmPptEY1IW6BxW5wpdvyi_RSZ5.QX1cjM1wSNxAzNzEzW}`

In the problem statement, it was provided that `/challenge/run` invokes `win` from `/challenge/more_commands`, so setting `PATH` to that directory enables `win`.
```
hacker@path~setting-path:$ PATH="/challenge/more_commands"
hacker@path~setting-path:$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{QjmPptEY1IW6BxW5wpdvyi_RSZ5.QX1cjM1wSNxAzNzEzW}
hacker@path~setting-path:~$
```

## What I learned

Learned to set `PATH` to a specific directory so bare commands in that directory become available.

## References

The problem statement provided was used as the reference.

# 3.FINDING COMMANDS

The challenge introduced using `which` to find the absolute path of a command in `PATH`.

## My Solve

**Flag:** `pwn.college{wQAIqzSbwwc3ahkBVkfQWDHKL5o.01NzEzNxwSNxAzNzEzW}`

In the problem statement, it was provided that `win` lives in a subdirectory; using `which win` gives its location, then `cd` and `cat` the flag.
```
hacker@path~finding-commands:$ which win
/challenge/paths/30688/win
hacker@path~finding-commands:$ cd /challenge/paths/30688
hacker@path~finding-commands:/challenge/paths/30688$ cat flag
pwn.college{wQAIqzSbwwc3ahkBVkfQWDHKL5o.01NzEzNxwSNxAzNzEzW}
hacker@path~finding-commands:~$
```

## What I learned

Learned to use `which` to discover the location of a command executable in `PATH`.

## References

The problem statement provided was used as the reference.

# 4. ADDING COMMANDS

The challenge introduced creating a custom script named `win`, adding its directory to `PATH`, and letting `/challenge/run` invoke it.

## My Solve

**Flag:** `pwn.college{c20A-krNTDxuYKZCRWcFmC6HhV1.QX2cjM1wSNxAzNzEzW}`

In the problem statement, it was provided to write a `win` script that cats `/flag`, make it executable, set `PATH` to its directory, then run `/challenge/run`.
```
hacker@path~adding-commands:$ nano win
hacker@path~adding-commands:$ chmod u+x win
hacker@path~adding-commands:$ PATH="~"
hacker@path~adding-commands:$ /challenge/run
Invoking 'win'....
pwn.college{c20A-krNTDxuYKZCRWcFmC6HhV1.QX2cjM1wSNxAzNzEzW}
hacker@path~adding-commands:~$
```

## What I learned

Learned to create custom commands, add their directory to `PATH`, and override expected executables.

## References

The problem statement provided was used as the reference.

# 5. HIJACKING COMMANDS

The challenge introduced writing a fake `rm` script to hijack calls to `rm` via `PATH`.

## My Solve

**Flag:** `pwn.college{sT0uagRGUk83lq09q2F7AgqVW9_.QX3cjM1wSNxAzNzEzW}`

In the problem statement, it was provided to create a fake `rm` script (e.g., `rm` that cats `/flag`), make it executable, set `PATH` to include its directory, then run `/challenge/run`.
```
hacker@path~hijacking-commands:$ nano rm
hacker@path~hijacking-commands:$ chmod u+x rm
hacker@path~hijacking-commands:$ PATH="~"
hacker@path~hijacking-commands:$ /challenge/run
Trying to remove /flag...
pwn.college{sT0uagRGUk83lq09q2F7AgqVW9_.QX3cjM1wSNxAzNzEzW}
hacker@path~hijacking-commands:~$
```
## What I learned

Learned to hijack privileged commands by placing fake executables earlier in `PATH`.

## References

The problem statement provided was used as the reference.
