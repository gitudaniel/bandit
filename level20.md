In this level there is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

Basically just open a connection to a certain port and pass in the password to that connection as text.

How I did it I had two terminals opened both sshed into bandit level 20.

On one command I opened a port and sent through the password.

On the other terminal I used the setuid and directed it to the same port as the one I opened earlier.

Two terminals were opened so that the connection stays open as the setuid command reads for the password.




Command: On terminal 1: echo "GbKksEFF4yrVs6il55v6gwY5aVje5f0j" | nc -l 4444
         On terminal 2: ./suconnect 4444

What think as echo as the literal echo. It returns what you give it. What we want to do is have it return that password string but have it displayed in the opened port 4444

nc is used for anything involving connections the -l is used to tell it to listen for anything that comes through.

run suconnect without any variables to find out what it does

If the password found is the password to level 20 you get the next password




password to level 21: gE269g2h3mw3pwgrj0Ha9Uoqen1c9DGr
