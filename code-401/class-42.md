# magic method

Dunder methods let you emulate the behavior of built-in types.

 You can implement a `__getitem__` method which allows you to use Python’s list slicing syntax: `obj[start:stop]`.
 
 - Object Initialization: `__init__`
 - Object Representation: `__str__`, `__repr__`
    - __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

    - __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

>If you don’t want to hardcode "Account" as the name for the class you can also use self.__class__.__name__ to access it programmatically.

- Iteration: `__len__`, `__getitem__`, `__reversed__`

- Operator Overloading for Comparing Accounts: `__eq__`, `__lt__`
- Operator Overloading for Merging Accounts: `__add__`
- Callable Python Objects: `__call__`
- Context Manager Support and the With Statement: `__enter__`, `__exit__`
> A context manager is a simple “protocol” (or interface) that your object needs to follow so it can be used with the with statement. Basically all you need to do is add __enter__ and __exit__ methods to an object if you want it to function as a context manager.


# Iterators
Objects that support the __iter__ and __next__ dunder methods automatically work with for-in loops.

```python
class Repeater:
    def __init__(self, value):
        self.value = value

    def __iter__(self):
        return RepeaterIterator(self)

class RepeaterIterator:
    def __init__(self, source):
        self.source = source

    def __next__(self):
        return self.source.value
```


# Generators 
generators look like regular functions but instead of using the return statement, they use yield to pass data back to the caller.

when a return statement is invoked inside a function, it permanently passes control back to the caller of the function. When a yield
is invoked, it also passes control back to the caller of the function—but it only does so temporarily.

*Whereas a return statement disposes of a function’s local state, a yield statement suspends the function and retains its local state.*



