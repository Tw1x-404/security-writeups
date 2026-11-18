# Bandit Level 1 → 2

## Task
The password is stored in a file called - (a single dash)
in the home directory.

## Commands used
ls, cat

## How I solved it
My first try was:

    cat -

It didn't work. The command just waited for input, because many Linux
programs treat - as "read from standard input" instead of a filename.

The fix is to give the full path to the file, so it is clearly a file
and not an option:

    cat ./-

./ means "in the current directory", so the shell passes the actual file.

## What I learned
Some characters have a special meaning on the command line. Adding ./
in front of a filename is a simple way to make sure it is treated as a file.
