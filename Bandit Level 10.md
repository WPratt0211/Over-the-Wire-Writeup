# Bandit Level 10

## Level Goal

The password for the next level is stored in the file data.txt
in one of the few human-readable strings, preceded by several ‘=’
characters.

## Commands You May Need to Solve This Level

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

## Solution

Like the other challenges, you'll need to complete the following:

- Make sure you're connected to the `bandit9` user using the credentials from the last challenge
- Find the password.
- Use the password to connect to the `bandit10` user

This one should be relatively simple as well. Based on the information we've been given, the file 
contains strings and binary, so we want to make sure we get rid of the binary and only look at what
we can understand.
First I attempted to view all of the strings, hoping that there would be few enough to be able to
determine the password from there. We can use `cat data.txt | strings` to accomplish that.

While this does technically work because we can go through the list and choose the ones that fit
the description of what we're looking for (strings that begin with '='), a better way would be to
use `grep` to only get the strings that fit that description. taking our previous command, we can
add ` | grep ^=` to select the strings that begin with '='.

This greatly shortened our list, we can can determine the password easily from there.

As always, if you're receiving errors, check your spelling, syntax, and the credentials that you're using.

## That's it for Level 10, thanks for reading!
