#######
Verilog 
#######

Assign values
=============

In Verilog numbers can be assigned with size or not. If it is not declared the size it defaults to 32 bits. Also you must choose the base of the number and the options are decimal, hexadecimal, octal and binary. If not specified the base it defaults to the decimal base.

Examples:

122 - Unsized number with no base, so it is a 32 bit wide number with the value 122 in the decimal base.

3'b010 - 3 bit wide with the value 010 in base two or 2 in decimal base.

8'hAA- 8 bit wide with the value AA in the hexadecimal base.

6'o77 - 6 bit wide with the value 77 in the octal base.

'b010 - 32 bit wide with the value 2 in the decimal base.

'd2 - Same as before.

Negative Numbers
================

Negative numbers are stored as compliment two and the minus sign must be included before the specification of size.

Example: 

-10'd5 10 bit number stored as complement two of 5.

10'd-5 Illegal representation.

Special number characters 
=========================

========= ============================  ===============
Character Function                      Example
_         used for readability          16'h15_ab_cd_ef
x or X    specify unknown bits          16'h15abx
z or z    specify high impedance value  16'hz
========= ============================  ===============

Arithmetic operators
====================

If a = 5, b=10, c=2b'01 and d = 2'b0Z .

========= ============================  ==================
Character Operation performed           Example
\+        Add                           b + c = 11
\-        Subtract                      b - c = 9, -b=-10
\\        Divide                        a * b = 50
\*        Multiply                      b / a = 2
%         Modulus                       b % a = 0
========= ============================  ==================