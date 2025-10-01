# MODULE7_SHELL_VARIABLES

# 1. PRINTING VARIABLES

The challenge introduced using `$` to print environment variables using echo.

## My Solve

**Flag:** `pwn.college{4jIbAaq_OpJalbGts1VtSa_kTU9.QX3UTN0wSNxAzNzEzW}`

In the problem statement, it was provided that echoing `$FLAG` would display the flag.
``` 
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{4jIbAaq_OpJalbGts1VtSa_kTU9.QX3UTN0wSNxAzNzEzW}
``` 

## What I learned

Learned to access and print the value of environment variables using `$` with echo.

## References

The problem statement provided was used as the reference.

# 2. SETTING VARIABLES

The challenge introduced assigning values to shell variables.

## My Solve

**Flag:** `pwn.college{kEYXnFOQmYJGTE6HrOF4qi9bB57.QX5UTN0wSNxAzNzEzW}`

In the problem statement, it was provided that setting `PWN=COLLEGE` would yield the flag.
``` 
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{kEYXnFOQmYJGTE6HrOF4qi9bB57.QX5UTN0wSNxAzNzEzW}
``` 

## What I learned

Learned to assign values to shell variables using `=`.

## References

The problem statement provided was used as the reference.

# 3. MULTI-WORD VARIABLES

The challenge introduced quoting values with spaces.

## My Solve

**Flag:** `pwn.college{Qcv3Sb5grIYCjhopJzPywkPeKko.QXwYTN0wSNxAzNzEzW}`

In the problem statement, it was provided that `PWN="COLLEGE YEAH"` would yield the flag.
``` 
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Qcv3Sb5grIYCjhopJzPywkPeKko.QXwYTN0wSNxAzNzEzW}
``` 

## What I learned

Learned to quote variable values containing whitespaces via 'quoting'.

## References

The problem statement provided was used as the reference.

# 4. EXPORTING VARIABLES

The challenge introduced exporting variables to child processes.

## My Solve

**Flag:** `pwn.college{M8jclEAZRmRylJB-_0QVbnxaq47.QXyYTN0wSNxAzNzEzW}`

In the problem statement, it was provided that invoking /challenge/run with the PWN variable exported and set to the value COLLEGE, and the COLLEGE variable set to the value PWN but not exported would yield the flag.
``` 
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{M8jclEAZRmRylJB-_0QVbnxaq47.QXyYTN0wSNxAzNzEzW}
``` 

## What I learned

Learned to export variables for use by child processes with `export`.

## References

The problem statement provided was used as the reference.

# 5. PRINTING EXPORTED VARIABLES

The challenge introduced listing environment variables with `env`.

## My Solve

**Flag:** `pwn.college{Qs-5V6xk37ZO0ZfCUbLUEdpFInH.QX4UTN0wSNxAzNzEzW}`

In the problem statement, it was provided that running `env` would show the `FLAG` variable with its value.
``` 
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=b05fd895bd9b5035804194f36dd12ffa5541cbe3a0e9507f48bf2f2a1ee65876
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{Qs-5V6xk37ZO0ZfCUbLUEdpFInH.QX4UTN0wSNxAzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
``` 
## What I learned

Learned to list all exported environment variables using `env`.

## References

The problem statement provided was used as the reference.

# 6. STORING COMMAND OUTPUT

The challenge introduced command substitution with `$(...)`.

## My Solve

**Flag:** `pwn.college{sQWY8FBcP-pmEmA5WbNg-cTk4rB.QX1cDN1wSNxAzNzEzW}`

In the problem statement, it was provided that reading the output of the /challenge/run command directly into a variable called PWN would yield the flag.
``` 
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo "$PWN"
pwn.college{sQWY8FBcP-pmEmA5WbNg-cTk4rB.QX1cDN1wSNxAzNzEzW}
``` 

## What I learned

Learned to capture command output into variables using `VAR=$(command)`.

## References

The problem statement provided was used as the reference.

# 7. READING INPUT

The challenge introduced the `read` builtin to prompt for input.

## My Solve

**Flag:** `pwn.college{gtbo5lMqB-iI141gqQhWqBzXj94.QX4cTN0wSNxAzNzEzW}`

In the problem statement, it was provided that using read to set the PWN variable to the value COLLEGE would yield the flag.
``` 
hacker@variables~reading-input:~$ read -p "Enter value: " PWN
Enter value: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{gtbo5lMqB-iI141gqQhWqBzXj94.QX4cTN0wSNxAzNzEzW}
``` 

## What I learned

Learned to prompt and read user input into variables using `read -p`.

## References

The problem statement provided was used as the reference.

# 8. READING FILES

The challenge introduced redirecting file content into `read`.

## My Solve

**Flag:** `pwn.college{ErUaAZ3EmIZFVF83MV3YSByJt2-.QXwIDO0wSNxAzNzEzW}`

In the problem statement, it was provided that reading /challenge/read_me into the PWN environment variable would read the value and yield the flag.
``` 
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{ErUaAZ3EmIZFVF83MV3YSByJt2-.QXwIDO0wSNxAzNzEzW}
``` 

## What I learned

Learned to redirect file contents into `read VAR` using `<`.

## References

The problem statement provided was used as the reference.
