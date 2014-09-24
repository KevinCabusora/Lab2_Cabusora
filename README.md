Lab2_Cabusora
=============

Super Top Secret Cryptography Machine

#Objectives

Using subroutines, create a code that can decrypt a message using a key, and then store the result in RAM.

#Prelab

##Considerations
For this lab, we will be using a byte length key.  We have a message we wish to decrypt, and the hints given are to use the XOR function and to implement the code utilizing subroutines.

There were two subroutines provided with specific functions:

* Decrypt a character
* Decrypt entire message

In the lab notes it was explained that the XOR was to be used to decrypt the program.  The basic idea is to XOR a a byte of the data with the key (which encrypts the data).  The decryption (which we are concerned with) involves XORing the result of the first process.

# Pseudocode

## Main Loop

Move message into r5

Store value #0x200 into r4

Move key into r6

Call decryptMessage

End with forever loop

## decryptMessage

Move the first byte of r5 into r7

Call decryptCharacter

Move the resultant value from r7 into the memory address of r4

Increment where we are looking in r4

Loop back to the beginning

Pop return location off stack into PC

## decryptCharacter

Use XOR function with the key in r6 against the value currently in r7

Pop return location off stack into PC

# Testing

## Basic Functionality

On 19 September 2014 Dr. York tested my code.

The simplest way to check if the code worked was to run the code completely, then to check the output in the memory browswer.  I switched the output to display ASCII. 

The result was: Congratulations!  You decrypted the ECE382 hidden message and achieved required functionality#
