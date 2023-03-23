# Bandit Level 9

## Level Goal

The password for the next level is stored in the file data.txt
and is the only line of text that occurs only once

## Commands You May Need to Solve This Level

`grep`, `sort`, `uniq`, `strings`, `base64`, `tr`, `tar`, `gzip`, `bzip2`, `xxd`

## Helpful Reading Material

[Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)

## Solution

This one is also relatively simple, however, I wasn't sure how to do it. The reading material wasn't helpful
for actually finding the password (unless I missed something), so I did my own research by looking up how to
list only unique lines in a file. This seemed simple enough, and included using a command that was included
in the list of commands we may need.

All we have to do is sort the file and then print out the unique line. We cna do so by issuing the following command:
`sort data.txt | uniq -u`

Once we've done that, we should receive the string that we're looking for.

As always, if you're receiving errors, check your spelling, syntax, and the credentials that you're using.

## That's it for Level 9, thanks for reading!
