# 02. Function
Function is a block of code that performs a specific task multiple times without duplicating the any code. 
## How to define a function?
Observe the following the example.

    def add_three(input_var):
        output_var = input_var + 3
        return output_var
    
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

This prints a value of 528.0.

The number of hours may vary and can be passed through the calling function at the argument place to compute the salary after taxation.

## Advantages of Functions
1. Saves time as reduces the time by only calling the function with diffrent arguments instead of rewriting or duplicating the same codes multiple times.
2. Avoiding rewriting codes also avoids the errors (typo or otherwise).
3. Makes the program concise and hence efficient to debug.

**Caveat :** We should write the codes as little as possible to avoid the errors.

## Variable Scope

Variables defined inside the function body cannot be accessed outside of the function. For example, while printing ***pay_pretax*** and ***pay_aftertax*** outside the function throws error as "**NameError : name 'pay_aftertax' is not defined**".

Hence, we need to make sure that the information we need from the function must be mentioned in the return statement at the end of the function.

A variable's scope can be local or global. Variable that is defined inside a function has local scope of that function only and variable that is defined outside of all functions has global scope, hence they can be accessed anywhere.

## Functions with no arguments

We can define functions with no arguments as well where we just print statements without involving any calculations as shown in the following example.

    # Define the function with no arguments and with no return
    def print_hello():
        print("Hello, you!")
        print("Good morning!")
    
    # Call the function
    print_hello()

The output comes as 

    Hello, you!
    Good morning!

## Functions with multiple arguments

Thus far we have seen the examples of no argument and single argument functions. The multiple argument function is not much diffrent from single argument function except that multiple arguments are added within the parentheses in the function header and are separated by a comma.  

let's compute the same problem of single variable function again, but this time with multiple arguments where arguments will be **num_hours**, **hourly_wage** and **tax_bracket** where,
**num_hours** : number of hours worked in one week
**hourly_wage** : the hourly wage (in $/hour)
**tax_bracket** : percentage of your salary that is removed for taxes


Define the function as **get_pay_with_more_inputs()**.

> ***Defining the function***

        def get_pay_with_more_inputs(num_hours, hourly_wage, tax_bracket):
            # Pre-tax pay
            pay_pretax = num_hours * hourly_wage
            # After-tax pay
            pay_aftertax = pay_pretax * (1 - tax_bracket)
            return pay_aftertax

This time we need to pass 3 values, one value for each variable, separated by comma in the calling of the function.
Let's compute for 40 hours, $24/hour and 22% tax bracket.

> ***Calling the function***

        higher_pay_aftertax = get_pay_with_more_inputs(40, 24, .22)
        print(higher_pay_aftertax)

This returns a value of 748.8000000000001.
