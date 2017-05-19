The password is stored as one of the few human readable files beginning with =

Upon experimentation I found the data in the file is binary

Use strings to get the printable characters in the file and pipe the output to grep to filter according to the =

Command: strings data.txt | grep -e "^="

-e command is used to search for patterns

^ is regex to show it is at the beginning

password to level10: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
