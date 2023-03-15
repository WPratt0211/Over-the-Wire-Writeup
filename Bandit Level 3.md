# Bandit Level 3

## Level Goal

The password for the next level is stored in a file called spaces
in this filename located in the home directory

## Commands You May Need to Solve This Level

'ls', 'cd', 'cat', 'file', 'du', 'find'

## Helpful Reading Material

- [Google Search for "spaces in filename"](https://www.google.com/search?q=spaces+in+filename)

## Solution

Like the other challenges, you'll need to complete the following:

- Make sure you're connected to the `bandit2` user using the credentials from the last challenge
- Find the file in the home directory that contains the password. The filename is `spaces in this filename`
- Read the file and use the string to connect to the `bandit3` user

Since spacing is a common issue with filenamees, this one was easy since I often have to interact with files that have spaces in their names (more often than not due to my own filenaming oversight).
To my knowledge, there are two ways to accomplish this:

1. You can wrap the filename in double or single quotes (my preferred way) - `"spaced filename here"`
2. You can use a backslash to escape each space - `spaced\ filename\ here`

As always, if you're receiving errors, check your spelling, syntax, and the credentials that you're using. It may also be helpful to review the Reading Materials.

### That's it for level 3, thanks for reading!
