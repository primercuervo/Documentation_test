#############################
Verilog - Tasks and Functions
#############################

Tasks and functions are used to reduce code repetition. If your in your project you need to do something many times it is better to use a task or a function that will reduce code writing and it will be more readable.

Task
====
	
Tasks are subroutines that can be called anytime in the module they are defined, but it is possible to define them in a different file and include the file in the module. Task can include time delays, functions can't. Tasks can have any number of inputs and outputs, functions can have only one output. If a variable is declared within the task it is local to the task and can't be used outside the task. Tasks can drive global variables if no local variable are declared. Tasks are called with statements and cannot be used in a expression, functions can be used in a expression. Task example:

	
.. code-block:: Verilog
    
    module  task_calling (temp_a, temp_b, temp_c, temp_d);
    input [7:0] adc_a, adc_b;
    output [7:0] adc_a_conv, adc_b_conv;
    reg [7:0] temp_b, temp_d;

    task convert;
    input [7:0] adc_in;
    output [7:0] out;
    begin
        out = (9/5) *( adc_in + 32)
    end
    endtask
       	 
    always @ (adc_a)
    begin	
      convert (adc_a, adc_a_conv);
    end  
   
    always @ (adc_b)
    begin	
      convert (adc_b, adc_b_conv);
    end  
    	 
    endmodule

Functions
=========
	
Functions are like tasks, with some differences. Functions cannot drive more than one output and cannot have time delays. Some differences are:

- Functions cannot include timing delays, like posedge, negedge, # delay, which means that functions should be executed in "zero" time delay.
- Functions can have any number of inputs but only one output.
- The variables declared within the function are local to that function. 
- The order of declaration within the function defines how the variables passed to the function by the caller are used. 
- Functions can take, drive, and source global variables, when no local variables are used. When local variables are used, basically output is assigned only at the end of function execution.
- Functions can call other functions, but cannot call tasks.
	
.. code-block:: Verilog
    
    module simple_function();
   
    function  myfunction;
    input a, b, c, d;
    begin
        myfunction = ((a+b) + (c-d));
    end
    endfunction
                 
    input a, b, c, d, e ;
    output f;
    wire f;

    assign f =  (myfunction (a,b,c,d)) ? e :0;
      	 
    endmodule

References
==========

Verilog HDL Basics - Altera, ASIC World (http://www.asic-world.com/)