# Bandit Level 0

## Level Goal

The goal of this level is for you to log into the game using SSH.
The host to which you need to connect is
bandit.labs.overthewire.org, on port 2220.
The username is bandit0 and the password is bandit0. Once
logged in, go to the Level 1 page to find out how to beat Level
1.

## Commands you may need to solve this level

ssh

## Helpful Reading Material

- [Secure Shell on Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell)
- [How to use SSH on wikiHow](https://www.wikihow.com/Use-SSH)


## Solution

Since I am using Mac (and occasionally Bash on a Windows machine), my solutions will be using the Linux shell scripting syntax.

For this level, you'll need to complete the following steps:
- Open your Terminal or Command Prompt
- using ssh, type `ssh bandit0@bandit.labs.overthewire.org -p 2220`
- Once connected it will prompt you to type the given password.

If you're receiving errors, check your spelling, syntax, and the credentials that you're using. It may also be helpful to review the Reading Materials.

If you've connected successfully, you'll receive a message telling you to enjoy your stay.

### That's it for Level 0, thanks for reading!
