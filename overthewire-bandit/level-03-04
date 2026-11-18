# Bandit Level 3 → 4

## Task
The password is stored in a hidden file inside the `inhere` directory.

## Commands used
cd, ls, cat

## How I solved it
After navigating into the `inhere` directory with `cd inhere`, a standard `ls` showed nothing because hidden files are not displayed by default.

To find out how to show hidden files, I checked the built-in documentation (`ls --help` / `man ls`) and found the `-a` (all) flag:

    ls -a

This revealed the hidden file `...Hiding-From-You`. Finally, I read its contents using:

    cat ...Hiding-From-You

## What I learned
- In Linux, filenames starting with a dot (`.`) are hidden by default.
- `ls -a` lists all files in a directory, including hidden ones.
- Built-in documentation like `man <command>` and `<command> --help` are essential for quickly looking up available flags directly in the terminal.
