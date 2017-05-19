Here we need to find the line of text that occurs only once in the file data.txt

We first sort through the contents of a file to arrange its contents.

For more on this visit https://www.computerhope.com/unix/usort.html

We then pipe the sorted output to the uniq command

Uniq does not work on unsorted output because of multiple unconsecutive occurences of that value. In other words it does not keep track of any output and has no memory of what was previously matched.

Command: sort data.txt | uniq -u

The -u command prints out any unique output in the data

Password to level9: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
