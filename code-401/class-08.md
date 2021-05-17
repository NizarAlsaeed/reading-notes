# List Comprehensions

List comprehensions provide a concise way to create lists.List comprehensions provide a concise way to create lists.
It consists of brackets containing an expression followed by a for clause, then
zero or more for or if clauses.

```python
new_list = [expression(i) for i in old_list if filter(i)]
```

Example:
```python
# You can add more arguments:

>>> [x+y for x in [10,30,50] for y in [20,40,60]]
[30, 50, 70, 50, 70, 90, 70, 90, 110]
```

# Primer on Python Decorators
By definition, a decorator is a function that takes another function and extends the behavior of the latter function without explicitly modifying it.

Inner Functions

It’s possible to define functions inside other functions. Such functions are called inner functions.
```python

def parent():
    print("Printing from the parent() function")

    def first_child():
        print("Printing from the first_child() function")

    first_child()
```
>the inner functions are not defined until the parent function is called.
>But because of their local scope, they aren’t available outside of the parent() function.


`@my_decorator` is just an easier way of saying `say_whee = my_decorator(say_whee).` It’s how you apply a decorator to a function.


Example of a decorator:
```python
import functools

def decorator(func):
    @functools.wraps(func)
    def wrapper_decorator(*args, **kwargs):
        # Do something before
        value = func(*args, **kwargs)
        # Do something after
        return value
    return wrapper_decorator

```