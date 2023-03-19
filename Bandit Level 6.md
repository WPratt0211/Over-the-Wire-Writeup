# Bandit Level 6

## Level Goal

The password for the next level is stored in a file somewhere under
the inhere directory and has all of the following properties:

  human-readable
  1033 bytes in size
  not executable
  
## Commands You May Need to Solve This Level
  
`ls`, `cd`, `cat`, `file`, `du`, `find`

## Solution

Like the other challenges, you'll need to complete the following:

- Make sure you're connected to the `bandit5` user using the credentials from the last challenge
- Find the file that contains the password. The file is in the `inhere` directory
- Read the file and use the string to connect to the `bandit6` user

This one is a mess to look at. Once we're logged in and `cd` into the `inhere` directory, we can use `ls` to see what's in the directory.
It looks like there are twenty other directories inside this on, all containing a mixture of files and folders in them. I didn't see a way for the loop
to help us here, so I decided to try to use the `find` command. Since I haven't needed to use `find` a lot in my daily work, I needed to use `man find`
to learn more about the flags I can use to find exactly what I'm looking for based on the parameters given in the Level Goal.

I found that there are flags that we can use to specify the format, size, and executable status of the file using the `-type`, `-size`, and `-executable`
flags resepctively. 
We can use these like this:
`find -type f -size 1033c ! -executable`

Once that command is run, I get the file I'm looking for: `./maybehere07/.file2`

We can use `cat` to read the file and it contains a string that works for the password for the `bandit6` user.

As always, if you're receiving errors, check your spelling, syntax, and the credentials that you're using.

## That's it for Level 6, thanks for reading!
