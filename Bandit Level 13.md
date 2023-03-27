# Bandit Level 13

## Level Goal

The password for the next level is stored in the file data.txt,
which is a hexdump of a file that has been repeatedly compressed.
For this level it may be useful to create a directory under /tmp in
which you can work using mkdir. For example: mkdir /tmp/myname123.
Then copy the datafile using cp, and rename it using mv (read the
manpages!)

## Commands You May Need to Solve This Level

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`, `mkdir`, `cp`, `mv`, `file`

## Helpful Reading Material

[Hex dump on Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)

## Solution

Like the other challenges, you'll need to complete the following:

- Make sure you're connected to the `bandit12` user using the credentials from the last challenge
- Find the password.
- Use the password to connect to the `bandit13` user

