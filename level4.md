In this level the password for the next level is stored in the only human-readable file in the inhere directory.

What this tells us is that we need to know the file type and then know which files are easily read by humans.

This means using the file command. The file command determines the type of file




command: cd inhere
         ls
         file ./* (or alternatively file -- -*)
         cat

We first cd into the inhere directory and list the files (ls) to see what we're dealing with

We see that the files names are prefixed by a -

This means that the file names cannot be manipulated directly as it is

Dashed files can be manipulated by providing the full path (sauce: https://stackoverflow.com/questions/42187323/how-to-open-a-f-dashed-filename-using-terminal)

. means the current directory which is why it works

-- means end of all options this lets the command know that you're not feeding it a flag (sauce: http://www.unix.com/unix-for-dummies-questions-and-answers/11998-how-cat-file-name-starts.html look for #3)

This shows us that only one file is an ASCII text file. All the rest are data files. Humans do not read data files




password to level 5: koReBOKuIDDepwhWk7jZC0RTdopnAYKh
