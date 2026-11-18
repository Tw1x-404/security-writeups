# Bandit Level 0

## Task
Log into the game server via SSH. The host is bandit.labs.overthewire.org,
the port is 2220, and the username for this level is bandit0.

## Commands used
ssh

## How I solved it
SSH normally uses port 22, but this server runs on port 2220, so I had to
set the port with the -p option:

    ssh bandit0@bandit.labs.overthewire.org -p 2220

On the first connection SSH asked if I trust the server's fingerprint.
I confirmed with "yes" and then entered the password from the level page.

## What I learned
How to connect to a remote server with SSH, and that you can use -p to
connect on a port other than the default one.
