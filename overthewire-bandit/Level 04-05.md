# Bandit Level 4 → 5

## Task
The password is stored in the only human-readable file in the `inhere` directory.

## Commands used
cd, file, cat

## How I solved it
Inside the `inhere` directory, there were several files (`-file00` through `-file09`) whose names started with a dash. Instead of checking each file manually or looking for a specific filter flag, I used the `file` command combined with a wildcard (`*`) and `./` to inspect all of them at once without the leading dashes being treated as options:

    file ./*

Most files returned `data` (unreadable binary data), except for `-file07`, which was identified as `ASCII text`. I then read its contents using:

    cat ./-file07

## What I learned
- The `file` command determines the actual file type based on its contents, rather than printing the text itself or relying on file extensions.
- Wildcards like `*` allow running commands across multiple files simultaneously.
- Combining `./` with a wildcard (`./*`) safely handles multiple filenames starting with a dash (`-`).
