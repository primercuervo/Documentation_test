###########################################
Basics of Digital Systems - Boolean algebra
###########################################

***************
Boolean algebra
***************

It is a branch of algebra where the values of the variables are 0 and 1, or false and true respectively. There are only three operations, the logical conjunction denoted as ∧ or X, logical disjunction denoted as ∨ or + and logical negation denoted as ¬ or !. In this text we will use X, + and ! respectively as the logic gates and, or and negation. 

Axioms of Boolean algebra
=========================

From Wikipedia, *an axiom is a sentence or proposition that is not proven or demonstrated and is considered as obvious or as an initial consensus necessary for the construction or acceptance of a theory. For this reason, it is accepted as truth and serves as the starting point for deduction and inferences from other truths.* In Boolean algebra there are ten axioms and are described as follows. In these axioms “a” is a Boolean variable that can only assume 0 or 1.

========================                    =====================  
A1: a = 0 if a ≠ 1                           A6: a = 1 if a ≠ 0
A2: if a = 0 then !a = 1                     A7: if a = 1 then !a = 0 
A3: 0 X 0 = 0                                A8: 0 + 0 = 0
A4: 1 X 1 = 1                                A9: 1 + 1 = 1
A5: 0 X 1 = 1 X 0 = 0                        A10: 0 + 1 = 1 + 0 = 1
========================                    =====================  

Basic operations and Logic gates
================================ 

These axioms are the principles of the operations. We will see the three basic operations that are the AND, OR and NOT operations. For that we will use two Boolean variables a and b that can assume 0 and 1, or false and true.

For the construction of digital systems we use logic gates. There are three basic logic gates and others are formed with a combination of them. These gates can be realized in the real world with electronic circuits with transistors or FET’s.

AND operation
-------------

c = a AND b = a X b, 

We can do a table and calculate all possibilities for the result, this table is called the truth table. As this is a conjunction the result can only be true or 1 if a and b are true.

===    ===     ============
a	b	c = a AND b
===    ===     ============
0	0	0
0	1	0
1	0	0
1	1	1
===    ===     ============

AND Gate

.. image:: https://raw.githubusercontent.com/victorhkr/FPGA_examples_TEST/master/and_gate.png
    :height: 100px
    :width: 200 px
    :align: left

|
|
|
|
|

OR operation
------------

c = a OR b = a + b, 

For this disjunction operation the result is 1 if a or b is 1.

===    ===     ============
a	b	c = a OR b
===    ===     ============
0	0	0
0	1	1
1	0	1
1	1	1
===    ===     ============

OR Gate

.. image:: https://raw.githubusercontent.com/victorhkr/FPGA_examples_TEST/master/or_gate.png
    :height: 100px
    :width: 200 px
    :align: left

|
|
|
|
|

NOT operation
-------------

c = NOT a = !a, 

This negation operation changes the state of the variable.

===     ==========
a	c = NOT a 
0	1
1	0
===     ==========

NOT Gate

.. image:: https://raw.githubusercontent.com/victorhkr/FPGA_examples_TEST/master/not_gate.png
    :height: 100px
    :width: 200 px
    :align: left

|
|
|
|
|

Laws of Boolean algebra
=======================

The next laws offers tools to work with Boolean algebra, and many are seen in the normal algebra. These laws can simplify problems, digital circuits only doing the algebraic operations. This list of laws defines the Boolean algebra. They are described with the variables a, b and c and the Boolean operations.

- Associativity of +:                    a + (b + c) = (a + b) + c
- Associativity of X:                    a X (b X c) = (a X b) X c
- Commutativity of +:                    a + b = b + a
- Commutativity of X:                    a X b = b X a
- Distributivity of X over +:            a X (b + c) = (a X b) + (a X c)
- Identity for +:                        a + 0 = a
- Identity for X:                        a X 1 = a
- Annihilator for X:                     a X 0 = 0 
- Annihilator for +:                     a + 1 = 1 
- Idempotence of +:                      a + a = a
- Idempotence of X:                      a X a = a
- Absorption 1:                          a X (a + b) = a
- Absorption 2:                          a + (a X b) = a
- Distributivity of + over X:            a + (b X c) = (a + b) X (a + c)           
- Complementation 1:                     a X !a = 0
- Complementation 2:                     a + !a = 1      
- Double negation:                       !(!a) = a
- De Morgan 1:                           !a X !b = !(a + b)
- De Morgan 2:                           !a + !b = !(a X b)

From these laws you can note that there is a duality principle. If you change the operation + to X, or X to +, and 0 to 1, or vice versa the dual law can be obtained. 

Boolean functions
=================

A Boolean function is a function that has n variables or entries, so it has 2n possible combinations of the variables. These functions will assume only 0 or 1 in its output. An example of a Boolean function is this, f(a,b,c) = a X b + c. These functions are implemented with the logic gates.

Digital circuit of f(a,b,c)

.. image:: https://raw.githubusercontent.com/victorhkr/FPGA_examples_TEST/master/function.png
    :height: 200px
    :width: 400 px
    :align: left

|
|
|
|
|
|
|
|
|
 
Truth table of the function

===    ===     ===      ========
a	b	c	f(a,b,c)
===    ===     ===      ========
0	0	0	0
0	0	1	1
0	1	0	0
0	1	1	1
1	0	0	0
1	0	1	1
1	1	0	1
1	1	1	1
===    ===     ===      ========


There is a way to implement functions in a canonical form, the minimal form of a function. For example if we had to implement a function with the truth table of the function f. First we would form the terms where the function has value 1, with only one possible combination for every term. The term would be 1 for one combination of the entry and 0 to the others. To do that we would use an AND gate and make that combination with all inputs equal 1 in the AND gate. The function then would be a sum of all terms. So the terms of the truth table would be,

Terms of the ∑

===    ===     ===     =========        ===============
a	b	c	f(a,b,c)	Terms of the ∑
0	0	0	0	        0
0	0	1	1	        !a X !b X c
0	1	0	0	        0
0	1	1	1	        !a X b X c
1	0	0	0	        0
1	0	1	1	        a X !b X c
1	1	0	1	        a X b X !c
1	1	1	1	        a X b X c
===    ===     ===     =========        ===============

|
.. math::

    f (a,b,c) &= (!a X !b X c) + (!a X b X c) + (a X !b X c) + (a X b X !c) + (a X b X c) \\
              &= !b X c X ( a + !a) + b X c X ( a + !a ) + a X b X !c \\
              &= !b X c + b X c + a X b X !c \\
              &= c + a X b X !c \\
              &= (c + a X b) X ( c + !c) = a X b + c

With the laws of Boolean algebra it is done a simplification to implement the digital circuit with the less number of gates.  
There is another way to implement the canonical function, which is to implement the negated function and then negate again and use De Morgan laws to retrieve a product of terms. This is the dual form of the summatory. The function now will be a product of terms and the terms now will have the value 0 for one combination of the input and 1 for every other combination.

Terms of the ∏

== == == =========   ============ ======== =================
a  b  c  !f(a,b,c)	Terms     f(a,b,c) Terms of the ∏
== == == =========   ============ ======== =================
0  0  0  1	     !a X !b X !c 0	   a + b + c
0  0  1  0	     0	          1	   1
0  1  0  1	     !a X b X !c  0	   a + !b + c
0  1  1  0	     0	          1        1
1  0  0  1	     a X !b X !c  0	   !a + b + c
1  0  1  0	     0	          1        1
1  1  0  0	     0	          1        1
1  1  1  0           0	          1        1
== == == =========   ============ ======== =================

!f (a,b,c) = !a X !b X !c + !a X b X !c + a X !b X !c

!!f = f = !( !a X !b X !c + !a X b X !c + a X !b X !c) = !( !a X !b X !c) X !( !a X b X !c) X !( a X !b X !c)

= (a + b + c ) X (a X !b X c) X (!a X b X c)

Operating the terms we get the basic form that is f = a X b + c. 

The conclusion is that there are two ways to retrieve the canonical form of a function, which are the sum of the terms or its dual that is the product of the terms.
