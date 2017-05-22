This level was a bit tricky. You are given a range of ports from 31000 to 32000 all on localhost.

Of these ports you're supposed to find out which of these ports have a server listening on them, then find out which of those speak SSL and which don’t. Only one server will give you the next credentials.

This challenge requires nmap. nmap is a tool for scanning networks.

So you first need to find which servers are open and then find out which servers are speaking ssh.




Command: nmap -p 31000-32000 --version-intensity 1 localhost

The -p flag is used to search through a range of ports.

In this case port 31000 to port 32000.

--version-intensity 1 comes from this stackoverflow answer https://security.stackexchange.com/questions/55997/nmap-ssl-service-detection-how-to-check-all-open-ports-only-for-ssl-service

All these ports are on localhost

Once we have identified the ports we run the same command we ran on level 15 only changing the port number. For reference see (https://github.com/gitudaniel/bandit/commit/4e9023f0969d32845aa9de6c459919024fd9c976)

Only one of those port will give you credentials.

This is where it gets tricky because the correct port gives you an ssl private key.

I automatically thought to use ssh -i and create a file in the /home/bandit16 directory but I quickly found that I had no ability to make any changes to the system whatsoever.

Luckily we have the tmp directory in linux and we used it previously in level 12 (https://github.com/gitudaniel/bandit/blob/master/level12.md)

The files and folders in the /tmp/ directory are only required temporarily and therefore do not make any changes to the system. This gives you a lot of room to manipulate files.

Copy the contents of the private key you get back.

Create a directory under /tmp/ using mkdir and cd into it.

Create a file using vim and paste the contents there save the file.

Run the same command we ran in level 13 and voila you're in level 17

For future reference the password is below.

It was obtained by sshing as user bandit17 and readint the contents of the file bandit17 located in the directory /etc/bandit_pass/




password for level 17: xLYVMN9WE5zQ5vHacb0sZEVqbrp7nBTn
