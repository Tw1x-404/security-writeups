# Bandit Level 0 → 1

## Task
The password for the next level is stored in a file called readme
in the home directory.

## Commands used
ls, cat, exit, ssh

## How I solved it
After logging in, I listed the files in the home directory:

    ls

The file readme was there, so I printed its content:

    cat readme

That gave me the password for bandit1. I logged out with exit and
connected again as the next user:

    ssh bandit1@bandit.labs.overthewire.org -p 2220

## What I learned
The basic workflow for every level: look around with ls, read files
with cat, then log in as the next user with the password I found.
