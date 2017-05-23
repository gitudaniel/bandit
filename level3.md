In this file we need to read the contents of a hidden file.

To read a hidden file we need to find it first.

Luckily though the file itself is hidden it still consumes disk space.

To find how much disk space a file consumes use du which is short for disk usage

du shows you how much space each of the files and subdirectories in a directory consume.




command: du -ah inhere
         cat /home/bandit3/inhere/.hidden

run this command while still in the home directory.

-a flag lists all the files and subdirectories. It lists everything including hidden files

-h flag displays it in human readable format. This means it displays the size each file takes up (see https://www.tecmint.com/check-linux-disk-usage-of-files-and-directories/ for clarification)

inhere is the directory we're interested in

The output of this is two files one of which is called .hidden presented as /home/bandit3/inhere/.hidden

cat reads the contents of that file.




password to get to level 4: pIwrPrtPN36QITSp3EQaw936yaFoFgAB
