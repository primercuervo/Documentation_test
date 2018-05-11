#######################################################################
Basics of Digital Systems - Mathematical operations with the binary base
#######################################################################

********************************************
Mathematical operations with the binary base
********************************************

Operations with binary base are equal the decimal base. The difference is when we need to store numbers in a finite amount of bits. Let’s do some operations with 8 bits, where the MSB is the signal bit and the others 7 bits are the bits of numerical value.

Sum
===
104\ :sub:`10`\ + 2\ :sub:`10`\ = 0110 1000\ :sub:`2`\ + 0000 0010\ :sub:`2`\ = 0110 1010\ :sub:`2`\ = 106\ :sub:`10`\  

As the result isn’t greater than 0111 11112 , for this operation didn’t occurred overflow.

104\ :sub:`10`\ + 24\ :sub:`10`\ = 0110 1000\ :sub:`2`\ + 0001 1000\ :sub:`2`\ =  1000 0000\ :sub:`2`\ = 0\ :sub:`10`\  

As the result is greater than 0111 1111\ :sub:`2`\ the result is wrong and occurred overflow.

Subtraction
===========

-104\ :sub:`10`\ - 2\ :sub:`10`\ = -(104\ :sub:`10`\ + 2\ :sub:`10`\ )= -(0110 1000\ :sub:`2`\ + 0000 0010\ :sub:`2`\) = 1110 1010\ :sub:`2`\= - 106\ :sub:`10`\    

As the result isn’t greater than 0111 1111\ :sub:`2`\ , for this operation didn’t occurred overflow.

-104\ :sub:`10`\ - 24\ :sub:`10`\ = -(104\ :sub:`10`\ + 24\ :sub:`10`\ ) = -(0110 1000\ :sub:`2`\ + 0001 1000\ :sub:`2`\) = 1000 0000\ :sub:`2`\   

As the result is greater than 0111 1111\ :sub:`2`\  the result is wrong and occurred overflow.

-104\ :sub:`10`\ + 24\ :sub:`10`\ = -(104\ :sub:`10`\ - 24\ :sub:`10`\ ) = -(0110 1000\ :sub:`2`\ - 0001 1000\ :sub:`2`\) = 1101 0000\ :sub:`2`\   

Multiplication
==============

2\ :sub:`10`\ * 60\ :sub:`10`\ = 0000 0010\ :sub:`2`\ * 0011 1100\ :sub:`2`\ = 0111 1000\ :sub:`2`\ = 120\ :sub:`10`\
-2\ :sub:`10`\ * 60\ :sub:`10`\ = -0000 0010\ :sub:`2`\ * 0011 1100\ :sub:`2`\ = -0111 1000\ :sub:`2`\ = 1111 1000\ :sub:`2`\ = - 120\ :sub:`10`\

Division
========

60\ :sub:`10`\/2\ :sub:`10`\ = 0011 1100\ :sub:`2`\ / 0000 0010\ :sub:`2`\ = 0001 1110\ :sub:`2`\ = 30\ :sub:`10`\