In this level, use the find command with the parameters given.

The parameters given are the group user and file size

Note that bytes and characters are the same thing

Pass in / because you need to search through everything and everything belongs to root

Pass that output to grep to filter through the output

Use grep -v (inverse filter) to return output that doesn't have the parameters passed.

In this case we do not want anything with the permission in the output

Command: find / -user bandit7 -group bandit6 -size 33c -print0 | xargs -0 grep -v "Permission"

-print0 prevents any problems from filenames having spaces in them while running the find command

-0 is used by xargs to serve the same purpose as -print0 in find

Output: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
