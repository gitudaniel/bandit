This level is more or less the same as level 22. Only the commands in the shell script are different.

In the shell script under /usr/bin/ there are two variables myname and mytarget

myname variable is the user the command is to be run under

mytarget variable is the target file within the tmp directory we're supposed to read

The command under my name is
        whoami

This prints the user I am logged in as

The command under mytarget is
        echo I am user $myname | md5sum | cut -d ' ' -f 1

echo simply returns what you've given it and we pipe that through to md5sum to generate a hash. You'll notice that what's generated is a hash and a hyphen

We then pipe that through to cut to remove the hyphen.

The -d flag is the delimeter. What a delimeter does is specify a boundary. So we want to separate the hash and the hyphen.

The -f flag is the fields. This specifies what is to be printed. In this case we want to print out the first delimited character hence the 1 at the end. This leaves out the hyphen since that is the second character.

Refer to level 22 for first set of commands. The commands here assume you've already found the location of the bandit23 shell script and read it




Commands: echo I am user bandit23 | md5sum | cut -d ' ' -f 1
          cat /tmp/<result of above command>




password to level 23: jc1udXuA1tiHqjIsL8yaapX5XIAI6i0n          
