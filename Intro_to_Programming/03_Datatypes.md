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

Whenever we write a number with decimal points, Python automatically recognises it as a float even if there is, technicallay, no fraction part. E.g., 1., or 2.0, or 3.00 all of these are considered float by Python.
