# MODULE8_DATA_MANIPULATION

# 1. TRANSLATING CHARACTERS

The challenge introduced using `tr` to translate characters from standard input.

## My Solve

**Flag:** `pwn.college{4gaxgQbAitLldTDBP2r8PE5_qN8.01MxEzNxwSNxAzNzEzW}`

In the problem statement, it was provided that `/challenge/run` would print a case-swapped flag that needed to be undone using `tr`.
``` 
hacker@data~translating-characters:~$ /challenge/run | tr 'A-Za-z' 'a-zA-Z'
yOUR CASE-SWAPPED FLAG:
pwn.college{4gaxgQbAitLldTDBP2r8PE5_qN8.01MxEzNxwSNxAzNzEzW}
hacker@data~translating-characters:~$
``` 
## What I learned

Learned to translate character ranges using `tr 'A-Za-z' 'a-zA-Z'` to swap case.

## References

The problem statement provided was used as the reference.

# 2. DELETING CHARACTERS

The challenge introduced using `tr -d` to delete specific characters.

## My Solve

**Flag:** `pwn.college{UxQyndlmWSs1hPFMNdE0P6H96xk.0FNxEzNxwSNxAzNzEzW}`

In the problem statement, it was provided that the flag would contain decoy characters (`^` and `%`) that needed to be removed using `tr -d`.
``` 
hacker@data~deleting-characters:~$ /challenge/run | tr -d '^%'
Your character-stuffed flag:
pwn.college{UxQyndlmWSs1hPFMNdE0P6H96xk.0FNxEzNxwSNxAzNzEzW}
hacker@data~deleting-characters:~$
``` 

## What I learned

Learned to delete specific characters from input using `tr -d` with character list.

## References

The problem statement provided was used as the reference.

# 3. DELETING NEWLINES

The challenge introduced using escaped characters with `tr` to remove newlines.

## My Solve

**Flag:** `pwn.college{YFUe4RasXElvzvAciWD6rBsvsWI.0VNxEzNxwSNxAzNzEzW}`

In the problem statement, it was provided that the flag would be split across multiple lines and needed to be joined by deleting newlines.
``` 
hacker@data~deleting-newlines:~$ /challenge/run | tr -d '\n'
Your line-split flag: pwn.college{YFUe4RasXElvzvAciWD6rBsvsWI.0VNxEzNxwSNxAzNzEzW}
hacker@data~deleting-newlines:~$
``` 
## What I learned

Learned to delete newline characters using `tr -d '\n'` with escaped newline specification.

## References

The problem statement provided was used as the reference.

# 4. EXTRACTING THE FIRST LINES WITH HEAD

The challenge introduced using `head` to display the first few lines of input.

## My Solve

**Flag:** `pwn.college{IU0mjVY8pBOvba70ldLlAeZPys8.0lNxEzNxwSNxAzNzEzW}`
``` 
In the problem statement, it was provided that piping the first 7 lines from `/challenge/pwn` to `/challenge/college` would yield the flag.
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{IU0mjVY8pBOvba70ldLlAeZPys8.0lNxEzNxwSNxAzNzEzW}
hacker@data~extracting-the-first-lines-with-head:~$
``` 
## What I learned

Learned to extract specific number of lines from input using `head -n` with chained pipes.

## References

The problem statement provided was used as the reference.

# 5. EXTRACTING SPECIFIC SECTIONS OF TEXT

The challenge introduced using `cut` to extract specific columns from delimited data.

## My Solve

**Flag:** `pwn.college{UtFwjNwEaXhJAAKFfMupdIEx6Tw.01NxEzNxwSNxAzNzEzW}`
``` 
In the problem statement, it was provided that extracting the second column and removing newlines would reveal the flag.
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d '\n'
pwn.college{UtFwjNwEaXhJAAKFfMupdIEx6Tw.01NxEzNxwSNxAzNzEzW}
hacker@data~extracting-specific-sections-of-text:~$
``` 

## What I learned

Learned to extract specific columns using `cut -d` for delimiter and `-f` for field number.

## References

The problem statement provided was used as the reference.

# 6. SORTING DATA

The challenge introduced using `sort` to organize lines in alphabetical order.

## My Solve

**Flag:** `pwn.college{Qupc2F14yEFTZpp0O3wKpbAA9GZ.0FM0MDOxwSNxAzNzEzW}`

In the problem statement, it was provided that sorting `/challenge/flags.txt` alphabetically and extracting the last line would reveal the real flag.
``` 
hacker@data~sorting-data:~$ sort /challenge/flags.txt | tail -n 1
pwn.college{Qupc2F14yEFTZpp0O3wKpbAA9GZ.0FM0MDOxwSNxAzNzEzW}
hacker@data~sorting-data:~$
``` 

## What I learned

Learned to sort file contents alphabetically using `sort` and extract the last line with `tail -n 1`.

## References

The problem statement provided was used as the reference.

