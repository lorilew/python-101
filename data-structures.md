# Data Structures
[Back](README.md)

## Lists
Lists are a collections of ordered objects. They can be any type and not all elements in the list need to be the same type. Lists can be any size and can are mutable (can be changed). Be careful when you think you are copying a list, because if you have not done it properly you may have some unexpected results. 

To access an element in a list you need to use it's index. For lists the first index is 0.

```
>>> a = [1, "foo", 3, "bar", True]

>>> b = [1, "foo", 3, "bar", True]

>>> a == b
True

>>> a is b
False

>>> len(a)
5

>>> a[3]
"bar"

>>> a[-2]
"bar"

>>> "foo" in a
True
```

You can also slice lists. Try it out. 

```
>>> a = [1, "foo", 3, "bar", True]

>>> a[1:3]
["foo", 3]

>>> a[:3]
[1, "foo", 3]

>>> a[-3:]
[ 3, "bar", True]
```

Use slice to every other element.

```
>>> a[0:5:2]
[1, 3, True]
```

Use slicing to reverse a list.

```
>>> a[::-1]
[True, "bar", 3, "foo", 1]
```

There's lots more fun to have with lists. Refer to the link in _References_ below and try out some challenges. 

## Tuples

Tuples are similar to lists but they are immutable and are denoted by `()` instead of `[]`. To define a tuple of a single element you must remember the trailing `,`.

```
>>> t = ()
>>> type(t)
<class 'tuple'>

>>> name, age = ("foo", 4)
>>> name
"foo"

>>> u = ("goat",)
```

Accessing elements and slicing is done in the same way as lists. But remember tuples cannot be changed once defined.

## Dictionaries

## Sets

## Challenges
1. [Removing elements](https://www.codewars.com/kata/removing-elements/python)
2. [Manipulating Strings](https://www.codewars.com/kata/initialize-my-name/python)

## Quiz
[Python Lists and Tuples](https://realpython.com/quizzes/python-lists-tuples/)

### References
[Tuples & Lists](https://realpython.com/python-lists-tuples/)

[Dictionaries](https://realpython.com/python-dicts/)

[Sets](https://realpython.com/python-sets/)
