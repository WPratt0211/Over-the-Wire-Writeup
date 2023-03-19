# Bandit Level 5

##Level Goal

The password for the next level is stored in the only human-readable
file in the inhere directory. Tip: if your terminal is messed
up, try the “reset” command.

## Commands You May Need to Solve This Level

`ls`, `cd`, `cat`, `file`, `du`, `find`

## Solution

Like the other challenges, you'll need to complete the following:

- Make sure you're connected to the `bandit4` user using the credentials from the last challenge
- Find the file that contains the password. The file is in the `inhere` directory
- Read the file and use the string to connect to the `bandit5` user

This one can either be simple or complicated, depending on how you go about it. When you `cd` into the `inhere` directory and use `ls` to see the files,
you'll find that there are ten files with similar names, changing only the number at the end of the filename. For example, the first file is `-file00`.

The Level Goal explicitly stated that the password is contained in the only "human-readable" file. To determine that, we can just run the `file` command
against each file and it will tell us what kind of format the file is in.

Initially, I began to go through each file one-by-one, but after the third file I decided to do some research to see if there could be a way to automate
the process. I found that you can use loops in the terminal, so, after some syntax research, I tried that using the following:
`for i in {0..9}; do file ./-file0$i; done`

Presumably, this will create a `for-in` loop that will iterate over the files (starting with 0 and ending with 9) by creating a variable to use in the
place of the numbers at the end of the filename. We then plug that variable into the filenames that we need iterated over, and we end the loop when our
conditions are met.

This seems to have worked, and it told me that `-file07` contained ASCII text, which is human-readable. At this point, I used `cat` to read the file and
it contained a string that works as the password for the `bandit5` user.

As always, if you're receiving errors, check your spelling, syntax, and the credentials that you're using.

## That's it for Level 5, thanks for reading!
