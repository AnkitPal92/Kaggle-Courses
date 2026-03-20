# 02. Function
Function is a block of code that performs a specific task multiple times without duplicating the any code. 
## How to define a function?
Observe the following the example.

**def add_three(input_var):
    output_var = input_var + 3
    return output_var**
    
### Header
+ In the above block of code, the first line is called the '**header**' which specifies the name and arguments of the function. The rest of the code block is called the '**body**'.

+ The keyword '**def**' lets Python understand that a function is about to be defined, which followed by the name of the function, i.e., '**add_three**'. Immediately after the function name follows the argument(s), i.e., **input_var**" within a parentheses. The arguments are the name of the variables that will serve as the inputs to the function. A function can have no argument at all or multiple arguments.

+ The header is always terminated with a colon(:).

### Body
The function body specifies the work that function does.

+ Every line of code in the body of the function must be indented with exactly four spaces. This can be done by hitting the 'Tab' button once or pushing the space bar four times.
+ The function runs all the indented line of codes top to bottom by taking arguments as input. It stores the value after calculation in the output variable, i.e., '**output_var**'.
+ The last line of the code is called the '**return statement**' which returns the value stored in the output variable.

This above code cell only defines a function, but does not run it unless it is called. The 'calling of function' is described below.

## How to call(or run) a function?
Calling of a function is used interchangeably with running a function.

Let's understand the calling of function with the following example.

> Run the function with 10 as input

new_number = add_three(10)

> Check that the value is 13, as expected
> print(new_number)


