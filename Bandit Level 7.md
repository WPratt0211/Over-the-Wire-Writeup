# Bandit Level 7

## Level Goal

The password for the next level is stored somewhere on the
server and has all of the following properties:

  owned by user bandit7
  owned by group bandit6
  33 bytes in size
  
## Commands You May Need to Solve This Level

`ls`, `cd`, `cat`, `file`, `du`, `find`, `grep`

## Solution

Like the other challenges, you'll need to complete the following:

- Make sure you're connected to the `bandit6` user using the credentials from the last challenge
- Find the file that contains the password.
- Read the file and use the string to connect to the `bandit7` user

This one is quite a bit different from the others. Once we're logged in, we find that there are no files or folders in the home directory,
so we aren't immediately sure where to search. However, we can use the `find` command again to locate the file we're looking for.

Initially, I ran the following command:
`find / -user bandit7 -group bandit6 -size 33c`

However, that command produced too many errors and made the output difficult to interpret. So we can redirect the errors by adding `2>/dev/null`
so that we only get the output we're looking for.

Once we run that command, we are given a filepath:
`/var/lib/dpkg/info/bandit7.password`

We can use `cat` to read the file, and it contains the string used for the `bandit7` user password.

As always, if you're receiving errors, check your spelling, syntax, and the credentials that you're using.

## That's it for Level 7, thanks for reading!
