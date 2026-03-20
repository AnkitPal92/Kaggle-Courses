# 02. Function
Function is a block of code that performs a specific task multiple times without duplicating the any code. 
## How to define a function?
Observe the following the example.

    def add_three(input_var):
        output_var = input_var + 3
        return output_var**
    
### Header
+ In the above block of code, the first line is called the '**header**' which specifies the name and arguments of the function. The rest of the code block is called the '**body**'.

+ The keyword '***def***' lets Python understand that a function is about to be defined, which followed by the name of the function, i.e., '***add_three()***'. Immediately after the function name follows the argument(s), i.e., ***input_var***" within a parentheses. The arguments are the name of the variables that will serve as the inputs to the function. A function can have no argument at all or multiple arguments.

+ The header is always terminated with a colon (:).

### Body
The function body specifies the work that function does.

+ Every line of code in the body of the function must be indented with exactly four spaces. This can be done by hitting the 'Tab' button once or pushing the space bar four times.
+ The function runs all the indented line of codes top to bottom by taking arguments as input. It stores the value after calculation in the output variable, i.e., '***output_var***'.
+ The last line of the code is called the '***return statement***' which returns the value stored in the output variable.

This above code cell only defines a function, but does not run it unless it is called. The 'calling of function' is described below.

## How to call(or run) a function?
Calling of a function is used interchangeably with running a function.

Let's understand the calling of function with the following example.

    #Run the function with 10 as input
    new_number = add_three(10)
    
    #Check that the value is 13, as expected
    print(new_number)

Here **new_number** is the variable that is used to call/run the function ***add_three()*** with 10 as input and it stores the value which is returned by the function. The print statement publish the value of ***new_number***.

## Naming functions
Naming of functions should be done using lower case letters only with words separated by underscores instead of spaces. The name of a function should be chosen as a shorthand notations of the name of the task that a function performs, which could be inferred immediately from the name.

## A more complex example

Q) Determine a person's weekly paycheck after the taxes who falls under a 12% tax bracket ( i.e., 12% of his salary is taken for taxes and they only take home 88%) and he is paid $15/hour. The number of hours he worked is 40.

> **Defining the Function**

    def get_pay(num_hours):
    # Pre-tax pay, based on receiving $15/hour
    pay_pretax = num_hours * 15
    # After-tax pay, based on being in 12% tax bracket
    pay_aftertax = pay_pretax * (1 - .12)
    return pay_aftertax

> **Calling the Function**

    # Calculate pay based on working 40 hours
    pay_fulltime = get_pay(40)
    print(pay_fulltime)

The number of hours may vary and can be passed through the calling function at the argument place to compute the salary after taxation.

## Advantages of Functions
1. Saves time as reduces the time by only calling the function with diffrent arguments instead of rewriting or duplicating the same codes multiple times.
2. Avoiding rewriting codes also avoids the errors (typo or otherwise).
3. Makes the program concise and hence efficient to debug.

**Caveat:** We should write the codes as little as possible in order to avoid the errors.

## Variable Scope

Variables defined inside the function body cannot be accessed outside of the function. For example, while printing ***pay_pretax*** and ***pay_aftertax*** outside the function throws error as "**NameError: name 'pay_aftertax' is not defined**"
