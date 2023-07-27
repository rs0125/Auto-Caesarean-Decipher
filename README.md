# Auto-Caesarean-Decipher
Auto-Caesarean-Decipher is a Python program designed to automatically decipher English text that has been enciphered using the Caesar Cipher technique. The program utilizes language recognition to identify the correct decryption key by comparing the deciphered text against a large English word database.


## How it works

### Input Text:
The program prompts the user to input the enciphered paragraph as a string.
The input text is converted to lowercase for consistency in the decryption process.

### English Word Database:
The program reads a 474k English words text file ('words.txt'), which serves as the English word database. This database is used to determine the validity of words during decryption.


### Word Count in Enciphered Text:
The program calculates the word count in the enciphered text. This word count is later used to measure the accuracy of the language recognition process.

### Decryption Loop:
The program runs a loop from 0 to 25, corresponding to the 26 possible shifts in Caesar Cipher (26 is included to handle the no-shift scenario, i.e., plaintext).
For each shift value, the program performs the Caesar Cipher decryption and converts the deciphered text to lowercase.
The deciphered text is then split into individual words to prepare for language recognition.

### Language Recognition:
The program uses binary search to check each word in the deciphered text against the English word database.
If a word in the deciphered text is found in the database, it increments a counter (dcount).

### Decryption Success Criteria:
After checking all the words in the deciphered text, the program compares the value of dcount with 75% of the word count in the enciphered text.
If the number of recognized words (dcount) is greater than 75% of the word count in the enciphered text, the decryption process is considered successful.

### Final Decryption Output:
If the decryption is successful (i.e., the language recognition match is over 75% accurate), the program prints the final deciphered text.
If no successful decryption is found, the program terminates without producing any output.

### Word Database File Closure:
The program closes the 474k English words text file after the decryption process.

## Resources
