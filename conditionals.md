# Conditionals and Iterations
[Back](README.md)

## If/Else Statement

// todo

```
if "beer" in fridge:
    print("I'll have a beer")
elif "Cola":
    print("I'll have a cola")
else:
    print("Pass me my coat!")
```    

## For Iteration

This is a type of definite iterations.

```
>>> for i in range(5, 15, 3):
...  print(i)
...
5
8
11
14

a = [1, "foo", {"some-key": 4}, [1,2,3], ("bob", 56)]
>>> for el in a:
...     print(el)
... 
1
foo
{'some-key': 4}
[1, 2, 3]
('bob', 56)
```

If you would like to know the element index too you can use enumerate.

```
>>> a = [1, "foo", {"some-key": 4}, [1,2,3], ("bob", 56)]
>>> for i, x in enumerate(a):
...     print(f"{i}: {x}")
... 
0: 1
1: foo
2: {'some-key': 4}
3: [1, 2, 3]
4: ('bob', 56)
```
You can loop over any iterable; `String`, `List`, `Tuple`, `Set` and `Dict`. 

Looping through a `Dict` references the keys. If you want to access the values use `d.values()`; and to access the key, value pair use `d.items()`.

```
>>> for k,v in my_first_d.items():
...   print(f"{k}: {v}")
... 
name: Bob
age: 52
hair: none
```

## While Iteration

This type of iteration is indefinite. You need to set a condition for the while loop to continue, when the condition is no longer true the while loop will stop.

```
>>> n = 5
>>> while n > 0:
...     n -= 1
...     print(n)
...
```

You can use the key words `break` and `continue` to change the behaviour of the loop. `break` allows you to exit the loop early, and `continue` skips any code below the `continue` and  start the loop again.

You can use `else` at the end of a `while` loop to do an action when the loop terminates. The `else` statement will only run if the while loop terminates when the condition is exhausted, it will not run if the loop `break`s out.

## Challenges

1. [Are the numbers in order?](https://www.codewars.com/kata/are-the-numbers-in-order/train/python)

### References
[Real Python Conditional Statements](https://realpython.com/python-conditional-statements/)
