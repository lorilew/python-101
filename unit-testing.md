# Unit Testing
[Back](README.md)

Documentation
[unittest — Unit testing framework](https://docs.python.org/3/library/unittest.html)

Import TestCase and set up your test case class:
```
from unittest import TestCase

class UtilTestCase(TestCase):

   def test_this_thing_works(self):
      s = 'hello world'
      self.assertEqual(s.split(), ['hello', 'world'])
      
   def test_this_exception(self):
       # check that s.split fails when the separator is not a string
       with self.assertRaises(TypeError):
           s.split(2)
           

if __name__ == '__main__':
    unittest.main()           
```

To run the tests use:
```
python -m unittest test_module.TestClass.test_method
```

Using SetUp and TearDown Methods:
//todo

