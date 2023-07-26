# Auto-Caesarean-Decipher
A program that automatically deciphers english text enciphered in caesar cipher via language recognition


## How it works
The program is based on Caesar Cipher (similar to the one I had used in DiCipher)

The algorithm accepts a input text from the user as a string variable and then runs a singular letter shift on it. 
After that, the temp-decipher is split into words in a singular array.
Then a for loop checks each word through an english dictionary resource of 474k words (linked below)
If the language recognition match comprises of over 80% accuracy in terms of array length of valid characters, it breaks the loop and returns the final decipher.

## Resources
