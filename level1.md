This level involved reading from a dashed-file name.

The kernel sees - as a valid filename but cat treats is as a synonym for stdin 
(see https://www.computerhope.com/jargon/s/stdin.htm for definition of stdin)

To read the file we need to prefix it with a path ./ or ~/ will do.

./ makes the file executable so it will execute the file with the cat command

~ is short for /home/<user> so ~/- stands for /home/<user>/-

To get more information on this see https://unix.stackexchange.com/a/16364https://unix.stackexchange.com/a/16364





command: cat ./-





password to get to level 2: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
