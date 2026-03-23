# 03. Datatypes

Any variable created in Python has its corresponding datatype such as integer, float, boolean, string, tuple, dictionary, list, set etc.
Datatype determines what kind of operation can be performed with them. For instance, two integers or two floats or integer with float or float with integer can be divided.

E.g., 4/2, 5.6/2.0, 5/2.0, or 9.0/3 are possible, but "World"/"Man" is not considered a valid operation.
Therefore, the actions should match datatypes to avoid any error.

## Integer
These are the numbers without any fractional part. They can be positive(1, 2, 3, ...), negative(..., -3, -2, -1), or zero.
To know thw datatype of a variable **type()** function is used, shown as in the below example.

    x = 14
    print(x)
    print(type(x))
> 14

> <class 'int'>

<class 'int'> in the above output refers to integer datatype.

## Floats
Floats are numbers with fractional part. 

    nearly_pi = 3.141592653589793238462643383279502884197169399375105820974944
    print(nearly_pi)
    print(type(nearly_pi))

> 3.141592653589793

> <class 'float'>

Floats can also be specified with a fraction.

    almost_pi = 22/7
    print(almost_pi)
    print(type(almost_pi))

> 3.142857142857143

> <class 'float'>

We can also round off the decimal places to a specified number with **round()** function as shown in the below example.

    # Round to 5 decimal places
    rounded_pi = round(almost_pi, 5)
    print(rounded_pi)
    print(type(rounded_pi))

> 3.14286

> <class 'float'>

Whenever we write a number with decimal points, Python automatically recognises it as a float even if there is, technicallay, no fraction part. E.g., 1. or 2.0 or 3.00, all of these are considered float by Python.

Let's check with the following example.

    y_float = 1.
    print(y_float)
    print(type(y_float))

> 1.0

> <class 'float'>

## Booleans

Booleans are datatypes which represent one of two values(binary): True or False. 

    z_one = True
    print(z_one)
    print(type(z_one))

> True

> <class 'bool'>

Similarly, the variable can also be assigned with boolean value False. 

    z_two = False
    print(z_two)
    print(type(z_two))

> False

> <class 'bool'>

Booleans are particularly helpful when we require the truth value of an expression. 

    z_three = (1 < 2)
    print(z_three)
    print(type(z_three))

> True

> <class 'bool'>

In the above example, z_three took on a value True because the expression 1 < 2 was true.

Similarly, let's check for a flase statement with the following example.

    z_four = (5 < 3)
    print(z_four)
    print(type(z_four))

> False

> <class 'bool'>

Further, values of booleans can be altered by using **not** before them, like, **not True** is equivalent to **False**, and **not False** becomes **True**.
 Booleans becomes particularly crucial in conditionals, i.e, if else , for, while statements etc.

 ## Strings

It is a collection of characters (like alphabet letters, spaces, punctuations, numerical digits, or symbols) contained in quotation marks. They usually represent text.

    w = "Hello, Python!"
    print(w)
    print(type(w))

> Hello, Python!

> <class 'str'>

The length of a string can be determined using **len()** function. In the above example, the length of "Hello, Python!" is computed by taking into consideration the letters, comma, space and the exclamation mark which comes out to be 14.

    print(len(w))

> 14

The empty string is a special case, where the length is zero.

    shortest_string = ""
    print(type(shortest_string))
    print(len(shortest_string))

> <class 'str'>

> 0

Usually a number takes either an integer value or a float value, but if it is put inside quotation mark, it takes a string value as examined in the following example.

    my_number = "1.12321"
    print(my_number)
    print(type(my_number))

> 1.12321

> <class 'str'>

Note that, some strings are convertible to float and that can be done using **float()** function. For exapmle, "5.46395" and "6" can be converted to float.

***Caveat:*** Not every string is convertible to float datatype, like "Hello, Python!" cannot be converted to float.

    also_my_number = float(my_number)
    print(also_my_number)
    print(type(also_my_number))

> 1.12321

> <class 'float'>

Two strings can be added like we add two numbers (integer or float). In this case, the result is the concatenation of the two strings in the same order. 

    new_string = "World_" + "Hello"
    print(new_string)
    print(type(new_string))

> World_Hello

> <class 'str'>

Keep in mind that subtraction, division and multiplication are not viable operation between two strings.
However, multiplication of a string with an integer is possible and the result is the concatenation of the original string with itself a specified number of times as represented by the integer.

    newest_string = "abc" * 3
    print(newest_string)
    print(type(newest_string)

> abcabcabc

> <class 'str'>

***Caveat:*** Multiplication of string with a float returns an error.

    will_not_work = "abc" * 3.

> The error statement reads " TypeError: can't multiply sequence by non-int of type 'float' ".

