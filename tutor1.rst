################
Simple Examples
################

This will be a series of general topics about the concepts of digital systems and programmable logic. A digital system is a system formed by logic gates, which transforms logic input into a logic output with a logic function. Memories, processors, cellphones and all kind of electronics have digital circuits. The logic gates that are the building blocks of a digital system can be implemented with analog circuits and digital circuits, but with the advance of the semiconductor technology there are much more electronic circuits. These circuits are formed with transistors, MOSFETs, and passive components like resistors, capacitors and inductors. 
An ASIC (Application Specific Integrated Circuits) is digital circuit that is on the vast majority of the electronic devices. The company does a project of a digital circuit and then fabricates thousands of chips to sell in the market. They are smaller, consumes low power, but the initial project costs a lot of money and you cannot change the circuit when it is already fabricated. 
An FPGA (Field Programmable Gate Array) is an integrated circuit that can be programmed and reprogrammed in the field. It has many logic gates, registers, flip-flops and the user program it configuring the connections between them. The advantage of an FPGA is the versatility that it has for tests and for learning.

===================
Logical Information
===================

The information is represented by numbers written in a digital way. Why digital? When you have finite components to store information, it must be written digitally, that is what your calculator does. It always store a finite amount of numbers, so for infinite numbers like 5.444… and if your calculator has 3 significant digits it rounds to 5.44. Otherwise if you represent a number infinitely it is called to represented analogically, and that is the case of the infinity number 5.444… .

Logical representation of numbers

	We commonly store the numbers in a decimal base, because of our ten fingers. But the numbers can be represented in other bases like binary, octal and hexadecimal. These bases are multiple of two and have many advantages to be used. Our computers, processors and digital systems stores the numbers in a binary base. In a digital system the bases are represented by voltage levels, like 0, 3.3V, 5V. First let’s start with a decimal base. The algorism that has more value, the one that is written in the left are said as most significant algorism. The one of less value that is written in the right is the less significant algorism. In the binary base these names are called very often and the most significant algorism is the most significant bit (MSB) and the less significant algorism is the less significant bit (LSB).

============
Decimal base
============

0, 1, 2, 3, 4, 5, 6, 7, 8 and 9 forms the decimal base. To represent this base in an electrical system we would have ten different voltage levels. A number greater than nine and numbers smaller than one need others algorisms to be represented. For example let’s write the number 11.5.

1*101 + 1*100 + 5*10-1= 11.510

In base ten the number is wrote like this, 11.510.

===========
Binary base
===========

0 and 1 forms the binary base. These are called bits and if a number in this base has n algorisms then it is said that it have n bits. To represent this base in an electrical system we would have two different voltage levels. A number greater than one and smaller than one need more than one algorism to be represented. For example 11.510 in base two is represented as 1011.12,

1*23+0*22+1*21+1*20 + 1*2-1 = 1011.12 = 11.510

Multiplications and divisions in this base by two are simple. If you multiply by two you rotate the number to the left and if you divide by two you rotate it to the right, for example:

 (1*23+0*22+1*21+1*20 + 1*2-1)*2 = 1*24+0*23+1*22+1*21 + 1*20 = 101112 = 2310
(1*23+0*22+1*21+1*20 + 1*2-1)/2 = 1*22+0*21+1*20+1*2-1 + 1*2-2 =101.112 = 5.7510

==========
Octal base 
==========

0, 1, 2, 3, 4, 5, 6 and 7 forms the octal base. To represent this base in an electrical system we would have eight different voltage levels. A number greater than seven and smaller than one need more than one algorism to be represented. For example 11.510 in octal base is represented as 13.48,

1*23+0*22+1*21+1*20 + 1*2-1 + 0*2-2+0*2-3 =1*81 + (2+1)*80 + 4*8-1 = 1*81+3*20+4*8-1 = 13.48 = 11.510

As 8 is 23 you can group the algorisms in a number written in a binary base to form a number in a octal base.

Hexadecimal base

0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E and F forms the hexadecimal base. To represent this base in an electrical system we would have sixteen different voltage levels. A number greater than sixteen and smaller than one need more than one algorism to be represented. For example 11.510 in the hexadecimal base is represented as B.816,

1*23+0*22+1*21+1*20 + 1*2-1 + 0*2-2+0*2-3 + 0*2-4 =11*160 + 8*16-1 = B.816 = 11.510

In this case 11 quantities represent the letter B. As 16 is 24 you can group the algorisms in a number written in a binary base to form a number in a octal base.

=====================
A simple LED blinker
=====================

This is the simplest example – a hardware equivalent of the Hello World – LED blink. There is no need to know any 
hardware description language ( HDL ), like VHDL or verilog for this example.

More details can be found `here <http://antonpotocnik.com/?p=487360>`__.

====================
Knight Rider Lights
====================

This example introduces the basic concepts of FPGA programming, you  will get familiar with Verilog language which
will be used to create your own module. Testing will be done in Vivado’s simulator.

More details can be found `here <http://antonpotocnik.com/?p=488784>`__.

==========
Stopwatch
==========
This example shows how communication between the Linux processing system and the programmable logic works. 

More details can be found `here <http://antonpotocnik.com/?p=489265>`__.

==================
Frequency Counter
==================
This example demonstraits how to use Red Pitaya’s 125 Msamples/s 14-bit ADC and DAC peripherals with the FPGA.

More details can be found `here <http://antonpotocnik.com/?p=519284>`__.

================
Pulse generator
================

This example demonstraits how to build a simple pulse generator for the Red Pitaya. The design uses standard Xilinx IP
blocks and a custom Verilog core that outputs a signal valid that is driven high when the pulse is played on the DAC.

Pulse shape is stored in a Block RAM that can be written from Linux. ADC data is written in a FIFO that can be read 
from Linux. The FIFO only accepts ADC data when a pulse is played on the DAC.

More details can be found `here <https://www.koheron.com/blog/2016/10/13/pulse-generator.html>`__.

