# Basic Data Types

[Back](README.md)

## Numbers
There are two types of numbers in Python *Integers* and *Floating-Point*.

Integers are whole numbers and have no limit on size. Floating-point numbers are specified with a decimal point. You can also optionally use the character _e_ or _E_ to specify scientific notation. The maximum size of floating-point numbers is 1.8 ⨉ 10308.

```
>>> type(4)
<class 'int'>

>>> type(5.53223)
<class 'float'>

>>> type(.4)
<class 'float'>

>>> .4e7
4000000.0
```

## Strings
Strings are sequences of character data. String literals may be delimited using either single or double quotes (please be consistent - it looks terribly messy when you mix them). If you want to include quote characters in your string you can delimit your string with the other type of quote, see below for an example. Another way, but not recommended by Python's pep8 is to use escape sequences `\"`.

```
>>> print('Hi, there!')
Hi, there!

>>> print("Why, hello")
Why, hello

>>> print('Your hat is "interesting".')
Your hat is "interesting".

>>> print("Your shoes are...\n\"interesting\".")
Your shoes are...
"interesting".
```

In Python3 you can use _fstrings_ to format your strings.

```
>>> my_var = 5

>>> my_var
5

>>> print(f"This sentence has {my_var} s's in it.")
This sentence has 5 s's in it.
```

## Booleans
Objects of the Boolean type may have one of two values, `True` or `False`. In Python expressions that evaluate to `True` Boolean are described as _truthy_ and `False` as _falsy_.

## Challenges
1. [Numbers](https://www.codewars.com/kata/century-from-year/train/python)
2. [Numbers](https://www.codewars.com/kata/volume-of-a-cuboid/train/python)
3. [Numbers](https://www.codewars.com/kata/balanced-number-special-numbers-series-number-1/train/python)
4. [Using fstrings](https://www.codewars.com/kata/a-needle-in-the-haystack/train/python)

### References
[Real Python Data Types](https://realpython.com/python-data-types/)
