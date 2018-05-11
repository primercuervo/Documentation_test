###################################################################
Basics of Digital Systems - Digital Information and Numerical Bases
###################################################################

***************************************
Digital Information and Numerical Bases
***************************************

Digital Information
===================

The information is represented by numbers written in a digital way. Why digital? When you have finite components to store information, it must be written digitally, that is what your calculator does. It always store a finite amount of numbers, so for infinite numbers like 5.444… and if your calculator has 3 significant digits it rounds to 5.44. Otherwise if you represent a number infinitely it is called to represented analogically, and that is the case of the infinity number 5.444… .


Representation of numbers
=========================

We commonly store the numbers in a decimal base, because of our ten fingers. But the numbers can be represented in other bases like binary, octal and hexadecimal. These bases are multiple of two and have many advantages to be used. Our computers, processors and digital systems stores the numbers in a binary base. In a digital system the bases are represented by voltage levels, like 0, 3.3V, 5V. First let’s start with a decimal base. The algorism that has more value, the one that is written in the left are said as most significant algorism. The one of less value that is written in the right is the less significant algorism. In the binary base these names are called very often and the most significant algorism is the most significant bit (MSB) and the less significant algorism is the less significant bit (LSB).

Decimal base
------------

0, 1, 2, 3, 4, 5, 6, 7, 8 and 9 forms the decimal base. To represent this base in an electrical system we would have ten different voltage levels. A number greater than nine and numbers smaller than one need others algorisms to be represented. For example let’s write the number 11.5.

:math:`1*10^1 + 1*10^0 + 5*10^{-1}` =  11.5\ :sub:`10`\

In base ten the number is wrote like this, 11.5\ :sub:`10`\.

Binary base
-----------

0 and 1 forms the binary base. These are called bits and if a number in this base has n algorisms then it is said that it have n bits. To represent this base in an electrical system we would have two different voltage levels. A number greater than one and smaller than one need more than one algorism to be represented. For example 11.5\ :sub:`10`\  in base two is represented as 1011.1\ :sub:`2`\,

:math:`1*2^3+0*2^2+1*2^1+1*2^0 + 1*2^{-1}` = 1011.1\ :sub:`2`\ = 11.5\ :sub:`10`\

Multiplications and divisions in this base by two are simple. If you multiply by two you rotate the number to the left and if you divide by two you rotate it to the right, for example:

:math:`(1*2^3+0*2^2+1*2^1+1*2^0 + 1*2^{-1})*2 = 1*2^4+0*2^3+1*2^2+1*2^1 + 1*2^0 =` 10111\ :sub:`2`\  = 23\ :sub:`10`\

:math:`(1*2^3+0*2^2+1*2^1+1*2^0 + 1*2^{-1})/2 = 1*2^2+0*2^1+1*2^0+1*2^{-1} + 1*2^{-2} =`101.11\ :sub:`2`\  = 5.75\ :sub:`10`\
