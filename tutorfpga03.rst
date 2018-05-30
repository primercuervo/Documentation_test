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

For the FPGA, division and multiplication are very expensive and sometimes you cannot synthesize division. If you use Z or X for values the result is unknown. The operations treat the values as unsigned. If a = 5, b=10, c=2b'01 and d = 2'b0Z . 

========= ============================  ==================
Character Operation performed           Example
\+        Add                           b + c = 11
\-        Subtract                      b - c = 9, -b=-10
\/        Divide                        a * b = 50
\*        Multiply                      b / a = 2
%         Modulus                       b % a = 0
========= ============================  ==================

Bitwise operators
=================

Each bit is operated, result is the size of the largest operand and  the smaller operand is left extended with zeroes to the size of the bigger operand. If a = 3'b101, b=3'b110 and c=3'b01X .

========= ============================  ==================
Character Operation performed           Example
\~        Invert each bit               ~a = 3'b010
\&        And each bit                  b & c = 3'b010
\|        Or each bit                   a | b = 3'b111
\^        Xor each bit                  a ^ b = 3'b011
\^~ or ~^ Xnor each bit                 a ^~ b = 3'b100
========= ============================  ==================

Reduction operators
===================

These operators reduces the vectors to only one bit. If there are the characters z and x the result can be a known value. If a = 5'b10101, b = 4'b0011, c = 3'bz00 and d = 3'bx011 .

========= ============================  ====================
Character Operation performed           Example
\&        And all bits                  &a = 1'b0, &d1'b0
\~&       Nand all bits                 ~&a = 1'b1
\|        Or all bits                   |a = 1'b1, |c = 1'bX
\~|       Nor all bits                  ~|a= 1'b0
^         Xor all bits                  ^a = 1'b1
\^~ or ~^ Xnor all bits                 ~^a = 1'b0
========= ============================  ====================

References
==========

Verilog HDL Basics - Altera