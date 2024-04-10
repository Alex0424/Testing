# Testing

this is a tutorial about: testing your or others python code

## Assert
assert is used to test a function for example: 
```
def square(x):
    return x + x

assert square(10) == 100
```
## Unit Testing

Unit testing is made for testing different types of code, so you dont have to rewrite tests over and over again, for example:

prime.py
```
import math

def is_prime(n):
    if n < 2:
        return False
    for i in range (2, int(math.sqrt(n)) + 1):
        if n % i == 0:
            return False
    return True
```
test1.py
```
import unittest

from prime import is_prime

class Tests(unittest.TestCase):

    def test_1(self):
        """check that 1 is not prime."""
        self.assertFalse(is_prime(1))

    def test_2(self):
        """check that 25 is not prime."""
        self.assertFalse(is_prime(25))

    def test_3(self):
        """check that 3 is prime."""
        self.assertTrue(is_prime(3))

    def test_4(self):
        """check that 5 is prime."""
        self.assertTrue(is_prime(5))

if __name__ == "__main__":
    unittest.main()
```

## Django Testing

coming soon

## Selenium Testing

coming soon