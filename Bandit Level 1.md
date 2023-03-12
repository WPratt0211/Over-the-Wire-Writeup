# Bandit Level 1

## Level Goal

The password for the next level is stored in a file called
readme located in the home directory. Use this password to log
into bandit1 using SSH. Whenever you find a password for a level,
use SSH (on port 2220) to log into that level and continue the game.

## Commands You May Need to Solve This Level

`ls`, `cd`, `cat`, `file`, `du`, `find`

## Solution

`ls` and `cat` were the only commands that I needed for this challenge. Using `ls`, I was able to find that there was a `readme` file in the home directory.
Using `cat`, I read the contents of the `readme` file, which was a string of seemingly random characters. Using those characters, I was able to log into the
bandit1 user.

### Note
I seemed to have issues switching users from bandit0 to bandit1, as each time I attempted to log into bandit1 from bandit0 I got authentication errors despite
using the provided password. I was able to fix this by simply logging out of the machine altogether and then logging into it straight to the bandit1 user
with the string in the `readme` file as the password.

### That's it for Level 1, thanks for reading!
