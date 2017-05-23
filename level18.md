In this challenge, someone has modified .bashrc to log you out when you log in with SSH.

This means that  once you enter the correct password to log in, you're successfully logged out.

What is needed is to open the readme file in the home directory.

We need to force ssh to open a new pseudoterminal but not point to /bin/bash (see https://askubuntu.com/a/141997 for more details on the differences between /bin/sh and /bin/bash)

The other option is /bin/sh

So we need to force ssh to open the default system shell (/bin/sh)

Note that for this level we need to ssh into bandit17 first before running any of the commands below




Command: ssh -t bandit18@localhost -p 2220
Then:    enter the password for level 18 and press Enter
Then:    ls to see what's in the home directory
Finally: cat readme




password to level 19: IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

