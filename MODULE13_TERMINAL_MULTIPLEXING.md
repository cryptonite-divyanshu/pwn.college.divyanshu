# MODULE13_TERMINAL_MULTIPLEXING

# 1. STARTING A SCREEN SESSION

The challenge introduced launching `screen` to enter a virtual terminal.

## My Solve

**Flag:** `pwn.college{Q6nNMf53qmYLOSWIcGg7mK-36Bo.0VN4IDOxwSNxAzNzEzW}`

In the problem statement, it was provided that simply running `screen` yields the flag.
```
hacker@dojo:~$ screen
Congratulations! You're inside a screen session!
Here's your flag:
pwn.college{Q6nNMf53qmYLOSWIcGg7mK-36Bo.0VN4IDOxwSNxAzNzEzW}
hacker@dojo:~$
```

## What I learned

Learned to start a Screen session by running `screen`.

## References

The problem statement provided was used as the reference.

# 2. DETACHING AND ATTACHING

The challenge introduced detaching with Ctrl-A d and reattaching with `screen -r`.

## My Solve

**Flag:** `pwn.college{8uiMxm6A1lZp8zxM7uoNvQIBNFy.0lN4IDOxwSNxAzNzEzW}`

In the problem statement, it was provided to detach from screen, run `/challenge/run`, then reattach.
```
hacker@terminal-multiplexing~detaching-and-attaching:$ screen
hacker@terminal-multiplexing~detaching-and-attaching:$ Ctrl-A d
[detached from ...]
hacker@terminal-multiplexing~detaching-and-attaching:$ /challenge/run
hacker@terminal-multiplexing~detaching-and-attaching:$ screen -r
Yes! Flag is: pwn.college{8uiMxm6A1lZp8zxM7uoNvQIBNFy.0lN4IDOxwSNxAzNzEzW}
hacker@terminal-multiplexing~detaching-and-attaching:~$
```

## What I learned

Learned to detach with **Ctrl-A d** and reattach with `screen -r`.

## References

The problem statement provided was used as the reference.

# 3. FINDING THE RIGHT SCREEN SESSION

The challenge introduced listing and selecting among multiple detached sessions with `screen -r`.

## My Solve

**Flag:** `pwn.college{4DXscS_ep3hjv4vm4sUj4Q_j6Q0.01N4IDOxwSNxAzNzEzW}`

In the problem statement, it was provided to try each session then run `screen -r` to reattach the correct one.
```
hacker@terminal-multiplexing~finding-sessions:$ screen -r 144.session_a702…
[detached]
hacker@terminal-multiplexing~finding-sessions:$ screen -r 150.session_1e1e…
[detached]
hacker@terminal-multiplexing~finding-sessions:$ screen -r 147.session_5135…
[detached]
hacker@terminal-multiplexing~finding-sessions:$ screen -r
Congratulations! You found the right session!
pwn.college{4DXscS_ep3hjv4vm4sUj4Q_j6Q0.01N4IDOxwSNxAzNzEzW}
hacker@terminal-multiplexing~finding-sessions:~$
```
## What I learned

Learned to reattach by specifying a session name or PID and find the correct session.

## References

The problem statement provided was used as the reference.

# 4. SWITCHING SCREEN WINDOWS

The challenge introduced multiple windows in one Screen session and switching with Ctrl-A 0/1.

## My Solve

**Flag:** `pwn.college{YNMo4At2tSrJcFnqS10Ig0KMoWc.0FO4IDOxwSNxAzNzEzW}`

In the problem statement, it was provided to attach, then use **Ctrl-A 0** to switch to Window 0.
```
hacker@terminal-multiplexing~switching-windows:$ screen -r
[attached]
Ctrl-A 1 shows welcome in window 1.
Ctrl-A 0
Here is your flag: pwn.college{YNMo4At2tSrJcFnqS10Ig0KMoWc.0FO4IDOxwSNxAzNzEzW}
hacker@terminal-multiplexing~switching-windows:~$
```

## What I learned

Learned to switch between windows in Screen with **Ctrl-A n/p/0–9**.

## References

The problem statement provided was used as the reference.

# 5. DETACHING AND ATTACHING WITH TMUX

The challenge introduced tmux’s detach (Ctrl-B d) and attach commands.

## My Solve

**Flag:** `pwn.college{8p3YfjKYqIhJBH53uIl6b1E1652.0VO4IDOxwSNxAzNzEzW}`

In the problem statement, it was provided to start `tmux`, detach with **Ctrl-B d**, run `/challenge/run`, then `tmux attach`.
```
hacker@terminal-multiplexing~detaching-and-attaching-tmux:$ tmux
[detached]
hacker@terminal-multiplexing~detaching-and-attaching-tmux:$ /challenge/run
Flag sent! Now reattach to your tmux session with: tmux attach
hacker@terminal-multiplexing~detaching-and-attaching-tmux:$ tmux attach
Congratulations, here is your flag: pwn.college{8p3YfjKYqIhJBH53uIl6b1E1652.0VO4IDOxwSNxAzNzEzW}
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$
```

## What I learned

Learned tmux detach with **Ctrl-B d** and reattach with `tmux attach`.

## References

The problem statement provided was used as the reference.

# 6. SWITCHING TMUX WINDOWS

The challenge introduced creating and navigating tmux windows with Ctrl-B c/n/p/0–9.

## My Solve

**Flag:** `pwn.college{cbbPDVy87U3YpOFrm5vWdg7oCRA.0FM5IDOxwSNxAzNzEzW}`

In the problem statement, it was provided that attaching to tmux and switching to Window 0 reveals the flag.
```
hacker@terminal-multiplexing~switching-windows-tmux:$ tmux
[status bar shows 0:*bash 1:bash]
Ctrl-B 0
Here is your flag: pwn.college{cbbPDVy87U3YpOFrm5vWdg7oCRA.0FM5IDOxwSNxAzNzEzW}
hacker@terminal-multiplexing~switching-windows-tmux:~$
```
## What I learned

Learned to navigate tmux windows with **Ctrl-B c/n/p/0–9** and use the status bar.

## References

The problem statement provided was used as the reference.

