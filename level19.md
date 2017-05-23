In this level we're given a setuid binary file in the home directory.

Once logged in run ls to see the binary file itself.

The site tells us to execute it without arguments to find out how to use it.

If you remember to execute a file in the current directory we add ./ before it to tell PATH to check in the current directory we're in for an executable file.
(see http://www.linfo.org/path_env_var.html for more details on PATH not to be confused with path)

It tells us that the binary file allows us to run the command as another user and gives the example   Example: ./bandit20-do id

Note bandit id gives us the various id's in use and bandit20-do only takes two arguments. I learnt this when I ran ./bandit20 id bandit20 cat /etc/bandit_pass/bandit20 and got the error id: extra operand 'cat'

Running ./bandit20-do id bandit20 temporarily sets the uid gid and groups to bandit 20. uid and gid stand for user id and group id respectively. Groups is the group that can commands

Running ./bandit20 alone however sets the euid to bandit 20. The euid is the effective user id. This is the user running commands. 

Since we know that ./bandit20 takes in 2 arguments and we need to print out an output of a given file we need to pass in as arguments a command to print out the contents of a file and the file to be printed out

The passwords are stored in the bandit_pass directory under /etc/ but can only be read as the user the file is named after. So we need to execute the command as a certain user. User bandit20 in this case.




Commands: ./bandit20-do
          ./bandit20-do id
          ./bandit20-do cat /etc/bandit_pass/bandit20





password to level 20: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
