# 03. Datatypes

Any variable created in Python has its corresponding datatype such as integer, float, boolean, string, tuple, dictionary, list, set etc.
Datatype determines what kind of operation can be performed with them. For instance, two integers or two floats or integer with float or float with integer can be divided. E.g., 4/2, 5.6/2.0, 5/2.0, or 9.0/3 are possible, but "World"/"Man" is not considered a valid operation.
Therefore, the actions should match datatypes to avoid any error.

## Integer
These are the numbers without any fractional part. They can be positive(1, 2, 3, ...), negative(..., -3, -2, -1), or zero.
To know thw datatype of a variable **type()** function is used, shown as in the below example.

    x = 14
    print(x)
    print(type(x))
> 14
> <class 'int'>
