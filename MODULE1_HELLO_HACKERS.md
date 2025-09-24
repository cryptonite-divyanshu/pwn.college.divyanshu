# MODULE1_HELLO_HACKERS
# 1. Intro to Commands
The challenge prompted me to invoke my first command on the bash script, 
The command `whoami` was introduced.

## My Solve
**Flag:** `pwn.college{g1u9TDIvT7sDN9R57-pIfOmlvWh.QX3YjM1wSNxAzNzEzW}`

In the problem statement, it was provided that, using the 'hello' command would provide the flag
```
hacker@hello~intro-to-commands:~$ whoami
hacker
hacker@hello~intro-to-commands:~$ hello
Success! Here is your flag:
pwn.college{g1u9TDIvT7sDN9R57-pIfOmlvWh.QX3YjM1wSNxAzNzEzW}
```

## What I learned
Learned that invoking just means to type the command and press enter.
I learnt to invoke my first command,
I learnt to invoke `whoami`,
The problem required me to run the command 'hello', which prompted me to the flag.

## References
The problem statement was the reference used.
```
Here, the user executed the whoami command, which simply prints the username (hacker) to the terminal. When the command terminates, the shell once again displays the prompt, ready for the next command.

In this level, invoke the hello command to get the flag! Keep in mind: commands in Linux are case sensitive: hello is different from HELLO.
```


# 2. Intro to Arguments
The challenge prompted me to use arguments with commands,
The command "echo" was introduced.

## My solve
**Flag:** `pwn.college{gFv2Q0HFeHGZobCyJ0OB1b0c6Dd.QX4YjM1wSNxAzNzEzW}`

I was provided in the problem statement that using the `hackers` argument with the `hello` command would prompt the flag.

```
hacker@hello~intro-to-arguments:~$ echo Hello
Hello
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{gFv2Q0HFeHGZobCyJ0OB1b0c6Dd.QX4YjM1wSNxAzNzEzW}
```

## What I learned
I leaned how to add arguments to commands,
I learned the use of echo command,
The problem required to me invoke the `hello` command with a specified argument to find the flag.

## References
The problem statement provided was used as the reference
```
Let's look at echo with multiple arguments:

hacker@dojo:~$ echo Hello Hackers!
Hello Hackers!
hacker@dojo:~$

In this case, the command was echo, and Hello and Hackers! were the two arguments to echo. Simple!

In this challenge, to get the flag, you must run the hello command (NOT the echo command) with a single argument of hackers. Try it now!
```


# 3. Command History
The challenge prompted me to check the command history. 

## My Solve
**Flag:** `pwn.college{IGOzjhxd4qa1Hqjkm3-6SHqnjqy.0lNzEzNxwSNxAzNzEzW}`

```
hacker@hello~command-history:~$ the flag is pwn.college{IGOzjhxd4qa1Hqjkm3-6SHqnjqy.0lNzEzNxwSNxAzNzEzW}
```

The flag was revealed after pressing `up arrow` key once.

## What I learned
I learned how to check command history,
By pressing, the `up` and `down` keys, I can jump back and forward between the already used commands.

## References
The problem statement was used as the reference
```
You're going to type a lot of commands, and typing everything from scratch can be annoying. Luckily, the shell saves a _history_ of every command you invoke.

You can scroll through those saved commands with the up/down arrow keys, and we'll practice that in this challenge. This challenge will inject the flag into your history. Bring up a terminal, hit the up arrow, and grab it! In other challenges, the history will contain the log of the commands you've run, so if you need to run a similar command again, you can use the arrow keys to scroll through and find it!
```
