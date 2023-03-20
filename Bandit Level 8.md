# Bandit Level 8

## Level Goal

The password for the next level is stored in the file data.txt
next to the word millionth

## Commands You May Need to Solve This Level

`man`, `grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

## Solution

Like the other challenges, you'll need to complete the following:

- Make sure you're connected to the `bandit7` user using the credentials from the last challenge
- Find the password.
- Use the password to connect to the `bandit8` user

This one was a bit of a relief after the last few. I'm unsure why they gave us so many new commands that we "may need" to solve the level.
Perhaps it was to throw us off, or perhaps there are mroe ways to complete this than I am aware of (which is entirely probable).

All we need to do here is use `ls` once logged in, and we can see that there is a `data.txt` file. When trying to read the file with `cat`,
we'll be greeted by a large, multi-line file with words paired with apparently random strings on each line. We could manually look for the word
that we need, "millionth", or we could just use `grep` to grab the line we need. Issue the following command:
`cat data.txt | grep millionth`

Our output should be the exact line we're looking for - the word "millionth" paired with our password. If we copy that string and use it to log
into the `bandit8` user, we'll find that it works.

As always, if you're receiving errors, check your spelling, syntax, and the credentials that you're using.

## That's it for Level 8, thanks for reading!
