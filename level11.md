In this exercise ROT13 is used.

This means that all the letters in the alphabet, both small and capital, are rotated by 13 letters.

From wikipedia(https://en.wikipedia.org/wiki/ROT13) rot13 is its own inverse.

The alphabet has 26 letters, rot13 splits that in half a-m and n-z.

The letters a-m are translated into the letters n-z and vice versa.

This means we need to use tr to reverse this translation.

tr does not work on files, or rather I was unable to make it work on the file data.txt out of the box.

What I did I read the file using cat and piped that output to tr.



Command: cat data.txt | tr a-zA-Z n-za-mN-ZA-M

a-zA-Z is the format of the data we are takin in

n-za-mN-ZA-M is how we want the data to be translated



Output: 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
