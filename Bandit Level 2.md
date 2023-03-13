# Bandit Level 2

## Level Goal

The password for the next level is stored in a file called - located in the home directory

## Commands You May Need to Solve This Level

`ls`, `cd`, `cat`, `file`, `du`, `find`

## Helpful Reading Material

- [Google Search for "dashed filename"](https://www.google.com/search?q=dashed+filename)
- [Advanced Bash-scripting guide - Chapter 3 - Special Characters](http://tldp.org/LDP/abs/html/special-chars.html)

## Solution

I didn't expect to get tripped up so early. However, since I'm not exactly a Linux administrator, I'm not _too_ disappointed in myself.
Just like in the last challenge, there is a file in the home directory of the user. However, this file is simply named `-`. This proved
to be a challenge, since that character is typically used to pass arguments with commands, so attempting to read the file with `cat -`
was ineffective.
After reviewing the reading material provided, I found two different options (let me know if you find any other ways around this):

1. You can use redirection `cat < -`
2. You can use the filepath `cat ./-`

Once you use one of the above commands, you should see another string of seemingly random characters. I once again was unable to switch
users due to receiving an authentication error (may be my fault somehow), so I simply logged out and logged into `bandit2@bandit.labs.overthewire.org`
and received my welcome message.

As Always, if you're still getting errors, make sure to check your spelling, syntax, and credentials.

### That's it for Level 2, thanks for reading!
