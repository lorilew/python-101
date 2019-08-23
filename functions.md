# Functions In Python
[Back](README.md)

In Python, functions are first-class objects. This means that you can treat a function like any 
other object and pass it around or use it as an arguament in another function.
```
>>> def add_one(number):
...    return number + 1
    
>>> print(add_one(4))
5
```

And a common mistake when starting out is forgetting the parenthesis. If you do not call the method
it won't do anything. In this example the print method is printing the object `add_one` that is of
type fuction.
```
>>> print(add_one)
<function add_one at 0x7f144112bbf8>
```

Here's an example of a function being passed as an arguement.
```
def good_feedback(name):
    return f"Hi {name}, you're doing a great job!"
    
def best_feedback(name):
    return f"Hey {name}, this is awesome!"
    
def give_feedback_bob(feedback_func):
    return feedback_func("Bob")
```
```
>>> give_bob_feedback(best_feedback)
"Hey Bob, this is awesome!"
```

Here's an example of a function being returned from another function
```
def present():
   return f"Wow, it's a Puppy"
   
def gift_present():
    return present
```
```
>>> new_present = gift_present()
>>> new_present()
"Wow, it's a puppy"
```

You can also define functions inside other functions. If you do this the inner functions will
only be inscope within the parent function and will not be able to be called from outside.

## Advanced Topics

### Decorators
Decorators wrap a function, modifying it's behaviour.

Example of using functions to wrap another function.
```
def go_on_rollacoaster():
    return "wwhhhheeeeeeeee!"

def check_height(fun_func):
    def wrapper():
        if height < 1.4:
            return "Sorry, you are too short to ride"
        else:
            return fun_func()
    return wrapper            

go_on_rollacoaster = check_height(go_on_rollacoaster)
```
```
>>> height = 1.2
>>> go_on_rollacoaster()
'Sorry, you are too short to ride'
>>> height = 1.8
>>> go_on_rollacoaster()
'wwhhhheeeeeeeee!'
```

In Python you can use decorators in a simpler way by using the `@` symbol. In this 
example you can see the decorator added to the `go_on_rollacoaster` function and there's no
need for the extra line redefining the original function.
```
def check_height(fun_func):
    def wrapper():
        if height < 1.4:
            return "Sorry, you are too short to ride"
        else:
            return fun_func()
    return wrapper            

@check_height
def go_on_rollacoaster():
    return "wwhhhheeeeeeeee!"
```
Decorators are useful for encapsulating repeated code that happens at the beginning or end of a
function. They also allow us to spearate concerns and test the repeated code once in it's own
function. A good example of this is checking that someone is authorised to use the function.

### References
https://realpython.com/primer-on-python-decorators/
