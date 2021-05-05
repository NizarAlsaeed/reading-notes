# Classes and Objects

Classes are a template to create your objects.

**Create a class:**

```python
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()
```

# Thinking Recursively
A recursive function is a function defined in terms of itself via self-referential expressions.

#### Recursive Data Structures in Python
A data structure is recursive if it can be deﬁned in terms of a smaller version of itself.
List, set, tree, dictionary are recursive data structure.

we can stop unnecessarily recomputing values by caching the results using `lru_cache`.

to set it up :

```python
from functools import lru_cache
@lru_cache(maxsize=None)
```

# Python Testing with pytest: Fixtures and Coverage

### Coverage
"code coverage", checks that your tests have run all of the code.

to include code coverage with pytest :
download and install `pytest-cov` from PyPI

provide an argument to `--cov`, specifying which program(s) you want to test.
`pytest --cov=test_file`

Then you'll need to turn the coverage report into something human-readable.

such as `coverage html` This creates a directory called htmlcov.
