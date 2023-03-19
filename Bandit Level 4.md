# Bandit Level 4

## Level Goal

The password for the next level is stored in a hidden file in the
inhere directory.

## Commands You May Need to Solve This Level

`ls`, `cd`, `cat`, `file`, `du`, `find`

## Solution

Like the other challenges, you'll need to complete the following:

- Make sure you're connected to the `bandit3` user using the credentials from the last challenge
- Find the file that contains the password. The filename is `.hidden` in the `inhere` directory
- Read the file and use the string to connect to the `bandit4` user

This is also a relatively simple one. You'll find that there is a directory called `inhere`, but when you `cd` into it, there seems to be nothing. It seems that there must be a hidden file, so running the `ls` command as normal won't show it to us, and we can't open it with `cat` if we can't see it, because we don't know what it's called. There are two ways you could go about finding and opening the file:

1. Use the `find` command. I wouldn't recommend this method, as the `find` command typically takes arguments and if you don't give it any, it can return a **LOT** of files/directories depending on what is in your current working directory. (use `man find` to get more information on the use cases for `find`)
2. The cleaner and easier way - `ls -a`. The `ls` command will list the files in your current directory (or the directory that you supply as a filepath after the command if applicable). The `-a` flag tells the command not list **ALL** files in the directory, including hidden ones.

If you're aware of any other methods, let me know!

Once you find the file, camed `.hidden`, you can use `cat .hidden` to open it and retrieve the string that will be the password for the `bandit4` user.

As always, if you're receiving errors, check your spelling, syntax, and the credentials that you're using.

## That's it for Level 4, thanks for reading!
