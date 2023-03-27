# Bandit Level 12

## Level Goal

The password for the next level is stored in the file data.txt,
where all lowercase (a-z) and uppercase (A-Z) letters have been
rotated by 13 positions

## Commands You May Need to Solve This Level

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

## Helpful Reading Material

[Rot13 on Wikipedia](https://en.wikipedia.org/wiki/Rot13)

## Solution

Like the other challenges, you'll need to complete the following:

- Make sure you're connected to the `bandit11` user using the credentials from the last challenge
- Find the password.
- Use the password to connect to the `bandit12` user

This one was a bit tricky, since, to my knowledge, there are no built-in ways to decode a ROT13 algorithm,
and the reading material didn't give us any way to do so. Technically, we could just read the file with `cat`
and look up a decoding tool to paste the string we're given. However, even though that isn't technically "wrong",
it isn't the point of doing these challenges. So after some research, I was able to find that we can use the `tr`
command to change characters. With a bit of regex (ew), we can get what we're looking for with the following command:
`cat data.txt | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'`

That command will read the `data.txt` file and translate each character to one with an alphabetical shift value of 13.

As always, if you're receiving errors, check your spelling, syntax, and the credentials that you're using.

## That's it for Level 12, thanks for reading!
