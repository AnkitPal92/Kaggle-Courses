# 04. Condition and Conditionals

## Introduction

To begin with, let's consider an example of a function, **add_two()**, which adds two to the input. So, the output of the function changes depending on the input. For instance, **add_two(5)** returns a value 7(= 5 + 2) and **add_two(8)** returns 10(= 8 + 2). 
So, irrespective of the input the function adds two, i.e., the functions invariably performs the same action.

However, if we need to change the action of the function depending on the inputs, we require condtions that will tell the function how to act on the input. For example, if we need a function **add_five_or_seven()** that adds five if the input is less than 10, and adds seven if the input is 10 or more. Then **add_five_or_seven(1)** will return 6 (= 1 + 5), but **add_five_or_seven(11)** will return 18 (= 11 + 7).

## Conditions

Conditions are statements that are either **True** or **False**. Of all the all the available way in programming, comparison between two values is the simplest for writing conditions. For example, check if 4 is greater than 5.

    print(4 > 5)

> False

This is the direct way to check a condition. Python found this to be **False** because 4 is not greater than 5.

We can also comapre variables storing values instead of comparing values directly.

    var_one = 4
    var_two = 5
    
    print(var_one < 4)
    print(var_two >= var_one)

> False

>True

A list of common symbols that are used write a condition is given below:

| Symbol | Meaning |
| --- | --- |
| == | equals |
| != | does not equal |
| < | less than |
| <= | less than or equal to |
| > | greater than |
| >= | 	greater than or equal to |

***Caveat:*** Do not use = sign to check two values, instead use == sign.

var_one = 4 sets the value of var_one to 4, however
var_one == 4 checks if the value of var_one is 4.


## What is a Conditional ?
A conditional statement includes a qualification/condition that need to be satified to carry out a specified operation defined by a block of codes within a function. In essence, they modify the way a function runs, based on the condition. If the condition is satified, i.e., it evaluates to **True**, then the function is executed. If the condition evaluates to **False**, then the code block within the function is not run.

### "if" statements
The simplest type of conditional statement is an "if" statement. Let's observe the following example to understand how it works.

    def evaluate_temp(temp):
        # Set an initial message
        message = "Normal temperature."
        # Update value of message only if temperature greater than 38
        if temp > 38:
            message = "Fever!"
        return message

<ins>**Explanation:**</ins>

+ Initially, message is set to "Normal temperature".
+ Then, if temp > 38 is True (e.g., the body temperature is greater than 38°C), the message is updated to "Fever!". Otherwise, if temp > 38 is False, then the message is not updated.
+ Finally, message is returned by the function.

        print(evaluate_temp(37))

> Normal temperature.

Here, in the above code cell, when we passed the temperature as 37&deg; So, the message comes out to be "Normal temperature", because the temperature is less than 38°C (temp > 38 evaluates to False) in this case.

In the following example, if the temperature is instead 39°C, since this is greater than 38°C, the message is updated to "Fever!".

    print(evaluate_temp(39))

> Fever!

Observe, in the above example, there are two levels of indentations. The first level of indentation for the function and the second is for the 'if' statement. 

Note here that, since the retun statement is indented under 'if' statement, it always runs irespective of whether **temp > 38** is **True** or **False**. 

### "if ... else" statements

"else" statements are executed if a statement is false. So, the code under "if" statement is run when the statement is True, and the code under "else" statement is run when it is False.

