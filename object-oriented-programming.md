# Object Oriented Programming (OOP)

[Back](README.md)

OOP is a way to structure your code so that properties and behaviours are bundled into individual objects. The
reason you would use OOP is that it _encapsulates_ the complexity of details and allows you to visual the process at a higher
level.

Python does not enforce you use OOP.

## Classes

Classes are used to describe user-defined data structures. For example an _Book()_ class may have the attributes 
_title_, _price_ and methods _set_price()_.  

When you create and use a object this is called an _instance_ of the class. Primitive data structures such as numbers, strings and lists are objects too.

Example

```
class Book:
    
    # Initialise by setting instance attributes.
    def __init__(self, title, price):
        self.title = title
        self.price = price
``` 

```
>>> the_tiny_unicorn = Book(title="The Tiny Unicorn", price=7.00)
>>> the_pigmy_alpaca = Book(title="The Pigmy Alpaca's Adventures On The Moon", price=50.00)

>>> print(the_tiny_unicorn.title)
The Tiny Unicorn

```

The *_init__()* method is called automatically when you create a new _Book_ instance.

You can then access the object attributes using the `.` dot-notation.

An object of a class is a copy of a class with concrete values. An object can be used to store data and can be passed between functions. You can create multiple instances of a class and they will be independent from each other. 

## Advanced Topics

Inheritance and composition are both concepts in OOP to model relationships between two classes. They both allow you
to encapsulate code but in different ways.

### Inheritance

The **Inheritance** model represents an **is a** relationship. For example, a car **is a** vehicle.

If a child class has a **is a** relationship with the parent class then it is said to **extend** the parent class. 
The child class then inherits all the parent attributes and methods.

The example below shows **Car extends Vehicle**. It inherits the Vehicle attribute `num_wheels`.

```
>>> class Vehicle:
...     num_wheels = 1
... 
>>> class Car(Vehicle):
...    model = "mini"
... 
>>> my_car = Car()

>>> type(my_car)
<__main__.Car>

>>> my_car.num_wheels
1
```

### Composition

The **Composition** model represents a **has a** relationship. For example, a pug **has a** tail.

```
>>> class Tail:
...   def wag(self):
...      print("wagging")
... 
>>> class Pug:
...     tail = Tail()
... 
>>> peanut = Pug()

>>> peanut.tail.wag()
wagging
```

### Inheritance or Composition?

It is generally advised to use composition over inheritance as it creates less dependedancies. In the example above you can
see that _wag()_ explicitly derives from _Tail_ which is much more readable than inherited methods and attributes.

However, inheritance may be the correct answer for the job; read the link below for helpful guidelines on when to use either
of these OOP models.

## References
[RealPython Object Oriented Programming](https://realpython.com/python3-object-oriented-programming/)
