## Importing your functions 

[Back](README.md)

### Example
In this example we will create a very simple python class and test without using any python frameworks.

1. Create a project directory `my-awesome-project`. This will be the *package* name.
2. Inside the project directory create a directory `my_first_module` with an empty file called `__init__.py`. This is your first module. All other modules will follow this pattern.
3. Inside the project directory create another directory called `tests` with an empty file called `__init__.py`. This is where your test files will be kept. 
```
my-awesome-project
  ├── my_first_module
  │   ├── __init__.py
  └── tests
      ├── __init__.py
```
4. Inside `my_first_module` create a file called `do_things.py` with the following code:
```
def do_the_thing():
  print('Wooo, I'm doing a thing!')
  return true
``` 
5. Inside `tests` create a file called `test_do_things.y` with the following code:
```
import unittest
from my_first_module import do_things

class DoThingsTestCase(unittest.TestCase):

  def test_do_the_thing(self):
    self.assertTrue(do_things.do_the_thing())
```
6. To run the tests:
```
cd ~/my-awesome-project
python3 -m unittest
```
output:
```
Wooo, I'm doing a thing!
.
----------------------------------------------------------------------
Ran 1 test in 0.000s

OK
```

### Trouble Shooting
If you are having probems with the import try:
```
cd ~/my-awesome-project
PYTHONPATH=. python3 -m unittest
```
