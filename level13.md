For this level the password is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14

This means that to read the password you have to be logged in as user bandit14

You have no root access therefore you cannot create user bandit14 switch users then read the file. Believe me, I tried.

In your current directory you have a file called ssh.private

This is your private ssh key. This tells you that you need to use ssh to log in but you need to force ssh to use this private key to log in.

The private key never changes. Public keys may be derived differently but the private keys are always the same.

To force ssh to use this private key use the -i flag. What this simply does is tell ssh that this is what you should use to log in.

Note that you are loggin in to the same machine as user bandit 14

localhost is the machine you're working on.




command: ssh -i ./ssh.private bandit14@localhost -p 2220
then:    cat /etc/bandit_pass/bandit14

The ./ simply tells shell that ssh.private is an executable file located in the current working directory.

Remember that the port for this challenge is port 2220. No other port will work.

At this point you will realise that you are already logged in and may not need to read the password. Remember you will not always be logged in and may need to log into bandit14 directly. Hence the cat command




password to level 14: 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e
