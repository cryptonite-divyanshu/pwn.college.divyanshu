# MODULE12_CHAINING_COMMANDS

# 1. CHAINING WITH SEMICOLONS

The challenge introduced using `;` to run multiple commands sequentially.

## My Solve

**Flag:** `pwn.college{UzhTRWy29q5QP2XCMpSEzLrXLNO.QX1UDO0wSNxAzNzEzW}`

In the problem statement, it was provided that chaining `/challenge/pwn` and `/challenge/college` with `;` yields the flag.
``` 
hacker@chaining~chaining-with-semicolons:$ /challenge/pwn; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{UzhTRWy29q5QP2XCMpSEzLrXLNO.QX1UDO0wSNxAzNzEzW}
hacker@chaining~chaining-with-semicolons:~$
``` 

## What I learned

Learned to run multiple commands in sequence using `;`.

## References

The problem statement provided was used as the reference.

# 2. BUILDING ON SUCCESS

The challenge introduced using `&&` to run a second command only if the first succeeds.

## My Solve

**Flag:** `pwn.college{Y_oMgU-xwCUSo0PzyGBno3hUL80.0lM0MDOxwSNxAzNzEzW}`

In the problem statement, it was provided that chaining `/challenge/first-success && /challenge/second` yields the flag.
``` 
hacker@chaining~building-on-success:$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{Y_oMgU-xwCUSo0PzyGBno3hUL80.0lM0MDOxwSNxAzNzEzW}
hacker@chaining~building-on-success:~$
``` 

## What I learned

Learned to conditionally run a command only if the previous one succeeded using `&&`.

## References

The problem statement provided was used as the reference.

# 3. HANDLING FAILURE

The challenge introduced using `||` to run a second command only if the first fails.

## My Solve

**Flag:** `pwn.college{ki-3u-YuaPAqIuihaNwJaCV41JK.01M0MDOxwSNxAzNzEzW}`

In the problem statement, it was provided that chaining `/challenge/first-failure || /challenge/second` yields the flag.
``` 
hacker@chaining~handling-failure:$ /challenge/first-failure || /challenge/second
Nice chaining! Flag: pwn.college{ki-3u-YuaPAqIuihaNwJaCV41JK.01M0MDOxwSNxAzNzEzW}
hacker@chaining~handling-failure:~$
``` 

## What I learned

Learned to provide fallback commands on failure using `||`.

## References

The problem statement provided was used as the reference.

# 4. YOUR FIRST SHELL SCRIPT

The challenge introduced writing a shell script file and executing it with `bash`.

## My Solve

**Flag:** `pwn.college{EtKv3Ik7fo_Ndw0ie4YE7VQZihy.QXxcDO0wSNxAzNzEzW}`

In the problem statement, it was provided to write a script (`x.sh`) that runs `/challenge/pwn` and `/challenge/college`, then execute it with `bash x.sh`.
``` 
hacker@chaining~your-first-shell-script:$ nano x.sh
hacker@chaining~your-first-shell-script:$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{EtKv3Ik7fo_Ndw0ie4YE7VQZihy.QXxcDO0wSNxAzNzEzW}
hacker@chaining~your-first-shell-script:~$
``` 

## What I learned

Learned to create and run a basic shell script using `bash script.sh`.

## References

The problem statement provided was used as the reference.

# 5. REDIRECTING SCRIPT OUTPUT

The challenge introduced piping the output of a script into another command.

## My Solve

**Flag:** `pwn.college{86rYxwc_jtDKIhWCqg6ZZXf6saM.QX4ETO0wSNxAzNzEzW}`

In the problem statement, it was provided to pipe `bash x.sh` into `/challenge/solve`.
``` 
hacker@chaining~redirecting-script-output:$ bash x.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{86rYxwc_jtDKIhWCqg6ZZXf6saM.QX4ETO0wSNxAzNzEzW}
hacker@chaining~redirecting-script-output:~$
``` 

## What I learned

Learned to pipe a script’s output to another command using `|`.

## References

The problem statement provided was used as the reference.

# 6. EXECUTABLE SHELL SCRIPTS

The challenge introduced making a script executable and running it directly.

## My Solve

**Flag:** `pwn.college{UA4h-nrQJFps_pioWSC486ArQFk.QX0cjM1wSNxAzNzEzW}`

In the problem statement, it was provided to make a shellscript that would invoke /challenge/solve, make it executable, and run it without explicitly invoking bash.
``` 
hacker@chaining~executable-shell-scripts:$ nano x.sh
hacker@chaining~executable-shell-scripts:$ chmod u+x x.sh
hacker@chaining~executable-shell-scripts:$ ./x.sh
Congratulations on your shell script execution! Your flag:
pwn.college{UA4h-nrQJFps_pioWSC486ArQFk.QX0cjM1wSNxAzNzEzW}
hacker@chaining~executable-shell-scripts:~$
``` 

## What I learned

Learned to set executable permission and run a script directly with `./script.sh`.

## References

The problem statement provided was used as the reference.

# 7. UNDERSTANDING SHEBANGS

The challenge introduced adding a shebang line to specify the interpreter.

## My Solve

**Flag:** `pwn.college{gtiGbYKZcvmPpagjRQ3YDpJPacr.0VOzMDOxwSNxAzNzEzW}`

In the problem statement, it was provided to create `/home/hacker/solve.sh` with `#!/bin/bash`, make it executable, and run `/challenge/run`.
``` 
hacker@chaining~understanding-shebangs:$ nano solve.sh
hacker@chaining~understanding-shebangs:$ chmod u+x solve.sh
hacker@chaining~understanding-shebangs:$ /challenge/run
Testing your script…
Perfect! Your flag:
Flag: pwn.college{gtiGbYKZcvmPpagjRQ3YDpJPacr.0VOzMDOxwSNxAzNzEzW}
hacker@chaining~understanding-shebangs:~$
``` 

## What I learned

Learned to add `#!/bin/bash` at the top of a script to specify the interpreter.

## References

The problem statement provided was used as the reference.

# 8. SCRIPTING WITH ARGUMENTS

The challenge introduced handling positional parameters in a script.

## My Solve

**Flag:** `pwn.college{INrOzpF2zDi31H_rdl5mxtrgMNt.0VNzMDOxwSNxAzNzEzW}`

In the problem statement, it was provided to write `/home/hacker/solve.sh` that reverses two arguments and run `/challenge/run`.
``` 
hacker@chaining~scripting-with-arguments:$ nano solve.sh
hacker@chaining~scripting-with-arguments:$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{INrOzpF2zDi31H_rdl5mxtrgMNt.0VNzMDOxwSNxAzNzEzW}
hacker@chaining~scripting-with-arguments:~$
``` 
## What I learned

Learned to access `$1` and `$2` to handle positional arguments in a script.

## References

The problem statement provided was used as the reference.

# 9. SCRIPTING WITH CONDITIONALS

The challenge introduced using `if` to conditionally output based on an argument.

## My Solve

**Flag:** `pwn.college{8rKn1RXr0kR81SY7OjggI8kyHjn.0lNzMDOxwSNxAzNzEzW}`

In the problem statement, it was provided to write `solve.sh` that outputs “college” for “pwn” and nothing otherwise, then run `/challenge/run`.
``` 
hacker@chaining~scripting-with-conditionals:$ nano solve.sh
hacker@chaining~scripting-with-conditionals:$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{8rKn1RXr0kR81SY7OjggI8kyHjn.0lNzMDOxwSNxAzNzEzW}
hacker@chaining~scripting-with-conditionals:~$
``` 

## What I learned

Learned to use `if [ "$1" = "pwn" ]` to conditionally execute code in a script.

## References

The problem statement provided was used as the reference.

# 10. SCRIPTING WITH DEFAULT CASES

The challenge introduced `if/else` to provide a default output.

## My Solve

**Flag:** `pwn.college{MRqCXY4qx8rALChkZh1PMFGeMZB.01NzMDOxwSNxAzNzEzW}`

In the problem statement, it was provided to write `solve.sh` that outputs “college” for “pwn” and “nope” otherwise, then run `/challenge/run`.
``` 
hacker@chaining~scripting-with-default-cases:$ nano solve.sh
hacker@chaining~scripting-with-default-cases:$ /challenge/run
Correct! Your script properly handles the if/else conditions.
Here's your flag:
pwn.college{MRqCXY4qx8rALChkZh1PMFGeMZB.01NzMDOxwSNxAzNzEzW}
hacker@chaining~scripting-with-default-cases:~$
``` 

## What I learned

Learned to implement `if … else` branches in a shell script.

## References

The problem statement provided was used as the reference.

# 11. SCRIPTING WITH MULTIPLE CONDITIONS

The challenge introduced using `elif` to handle multiple cases.

## My Solve

**Flag:** `pwn.college{AtUWNQcoqWmap_cK5aferGA_huq.0FOzMDOxwSNxAzNzEzW}`

In the problem statement, it was provided to write `solve.sh` that handles three keywords and defaults to “unknown,” then run `/challenge/run`.
``` 
hacker@chaining~scripting-with-multiple-conditions:$ nano solve.sh
hacker@chaining~scripting-with-multiple-conditions:$ /challenge/run
Correct! Your script properly handles all the conditions with elif.
Here's your flag:
pwn.college{AtUWNQcoqWmap_cK5aferGA_huq.0FOzMDOxwSNxAzNzEzW}
hacker@chaining~scripting-with-multiple-conditions:~$
``` 

## What I learned

Learned to use `elif` for multiple conditional branches in Bash.

## References

The problem statement provided was used as the reference.

# 12. READING SHELL SCRIPTS

The challenge introduced examining a script’s source to discover a hardcoded secret.

## My Solve

**Flag:** `pwn.college{0wwJTb0PAJjVYZTykPpqvCS3B7u.0lMwgDOxwSNxAzNzEzW}`

In the problem statement, it was provided that `/challenge/run` contains the password check in its source; reading it reveals “hack the PLANET.”
``` 
hacker@chaining~reading-shell-scripts:$ cat /challenge/run
#!/opt/pwn.college/bash

read GUESS
if [ "$GUESS" == "hack the PLANET" ]
then
echo "CORRECT! Your flag:"
cat /flag
else
echo "Read the /challenge/run file to figure out the correct password!"
fi
hacker@chaining~reading-shell-scripts:$ /challenge/run
hack the PLANET
CORRECT! Your flag:
pwn.college{0wwJTb0PAJjVYZTykPpqvCS3B7u.0lMwgDOxwSNxAzNzEzW}
hacker@chaining~reading-shell-scripts:~$
``` 

## What I learned

Learned to inspect shell script source code to find hardcoded logic and secrets.

## References

The problem statement provided was used as the reference.



