# Object Oriented Programming (OOP)

[Back](README.md)

OOP is a way to structure your code so that properties and behaviours are bundled into individual objects. The
reason you would use OOP is that it _encapsulates_ the complexity of details and allows you to visual the process at a higher
level.

Python does not enforce you use OOP.

## Classes

Classes are used to describe user-defined data structures. For example an _Book()_ class may have the attributes 
_title_, _price_ and methods _set_price()_.  

When you create and use a object this is called an _instance_ of the class. An object of a class is a copy of a class
with concrete values. An object can be used to store data and can be passed between functions. You can create 
multiple instances of a class and they will be independent from each other. 

Primitive data structures such as numbers, strings and lists are objects too.

Example

```
class Book:
    
    # Initialise by setting instance attributes.
    def __init__(self, title, price):
        self.title = title
        self.price = price
``` 

```
the_tiny_unicorn = Book(title="The Tiny Unicorn", price=7.00)
the_pigme_alpaca = Book(title="The Pigme Alpaca's Adventures On The Moon", price=50.00)

my_books = [the_tiny_unicorn, the_pigme_alpaca]

```


