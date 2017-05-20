Here the password is located in a base64 encoded file

Simply decode the file and read the contents of the file




Command: base64 -d data.txt | cat

-d tells base64 that it is supposed to decode the file and data.txt is the file to be decoded

| is a pipe that pipes the output to cat so that we are able to view the contents of the file




password for level 11: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
