# Bandit Level 2 → 3

## Task
The password is stored in a file in the home directory whose name
contains spaces and starts with dashes: --spaces in this filename--

## Commands used
ls, cat

## How I solved it
Without quotes, the shell splits the name at every space and passes
several separate words to cat. So the filename needs quotes:

    cat "--spaces in this filename--"

That still failed, because the name starts with -- and cat read it as
an option. There are two ways around this:

    cat -- "--spaces in this filename--"
    cat ./"--spaces in this filename--"

The -- tells the command that no more options follow. The ./ works the
same way as in the previous level. Both gave me the password.

Tab completion also helps here: typing cat ./-- and pressing Tab fills
in the name with the correct escaping.

## What I learned
- Spaces separate arguments, so filenames with spaces need quotes
  or backslashes.
- Names starting with - can be mistaken for options. -- or ./ fixes that.
- Tab completion saves time and avoids typos.
