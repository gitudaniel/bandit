Here we're supposed to submit the password of the current level to port 30001 on localhost using SSL encryption.

This means using openssl which is a crypto toolkit implementing SSL and  TLS network protocols.

Since we need to connect to localhost which means using the s_client flag

s_client establishes a transparent connection to a remote server speaking SSL/TLS

We need to use the -ign_eof to prevent shutting down fo the connection when end of file is reached. ign_eof means ignore end of file.

If this command is not used you get "HEARTBEATING read R BLOCK read:errno=0"




command: openssl s_client -ign_eof -connect localhost:30001
then:    paste password for level 15




password for level 16: cluFn7wTiGryunymYOu4RcffSxQluehd
