In this exercise we are given a hexdump which is the result of multiple compressions.

At some point something will have to be decompressed a number of times

We convert the hexdump into its original binary format using xxd -r and get more information about it using file. The -r flag converts a hexdump into binary

The output of file is "data2.txt: gzip compressed data, was "data2.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression"

This means the file was compressed using gzip(Lempel-Ziv coding). To decompress it we'll have to rename the file to have a .gz at the end.

We use mv for this

From man gzip we find that the -d flag is used to decompress files

After decompression we find a filename data2

On running $file data2 we get "data2: bzip2 compressed data, block size = 900k"

This means that the file was compressed using bzip2(Burrows-Wheeler algorithm).

It should then have .bz or .bz2 at the end so we rename it and decompress using the -d flag.

Repeat this till file gives you the output "POSIX tar archive (GNU)"

This means that the file was compressed using tar. Change the name to have a .tar suffix using mv and decompress using the -xvf flag

-x means extract, v means verbose(tell me what's going on) and f means use archive file or the device archive

Repeat these processes until the file command tells you that the file contains ASCII text




Commands: xxd -r data.txt output.txt
          file output.txt
          mv -v output.txt output.gz
          gzip -dv output.gz
          mv -v <filename> <filename.bz2/filename.bz>
          bzip2 -dv <filename.bz2/filename.bz>
          mv -v <filename> <filename.tar>
          tar -xvf <filename.tar>

In xxd data.txt is the file to be converted and output.txt is what we want the converted file to be called.




password to level 13: 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL


