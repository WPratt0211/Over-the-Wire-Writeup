# Bandit Level 11

## Level Goal

The password for the next level is stored in the file data.txt,
which contains base64 encoded data

#Commands You May Need to Solve This Level

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

## Helpful Reading Material

[Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64)

## Solution

Like the other challenges, you'll need to complete the following:

- Make sure you're connected to the `bandit10` user using the credentials from the last challenge
- Find the password.
- Use the password to connect to the `bandit11` user

All we need to do for this one is decode the base64 text in the `data.txt` file. Using the command `base64` that they gave us, we can pass the `-d`
flag, and we will get the pasword we need. Use the following command:
`cat data.txt | base64 -d`

As always, if you're receiving errors, check your spelling, syntax, and the credentials that you're using.

## That's it for Level 11, thanks for reading!
