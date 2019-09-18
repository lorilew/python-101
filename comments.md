# Comments in code

[Back](README.md)

I would like to start by saying that you do not always need to comment your code, but your code should be always readable. 
This page will describe the ways you can comment your code.

## Comment

Single line comments in Python use the `#` symbol. 

```
def add_one(arr):
    # Appends the number 1 to the end of the list
    return arr + [1]
```

Pep8 standard state that a comment should be no longer than 72 characters. If your comment exceeds this you should
comment on multiple lines. 

```
def function_with_complicated_code(x):
    # this is a really long comment that just
    # keeps going over multiple lines. It describes
    # a function that returns the same argument that gets passed
    # to it
    return x
```

