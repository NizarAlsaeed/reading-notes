# Python Scope & the LEGB Rule: Resolving Names in Your Code

scope determines the visibility of a variable within the code.
 The Python scope concept is generally presented using a rule known as the *LEGB* rule (Local, Enclosing, Global, and Built-in ).

 

Global scope: The names that you define in this scope are available to all your code.

Local scope: The names that you define in this scope are only available or visible to the code within the scope.


## Using the LEGB Rule for Python Scope
- **Local** (or function) scope is the code block or body of any Python function or lambda expression.

- **Enclosing** (or nonlocal) scope is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.

- **Global** (or module) scope is the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.

- **Built-in** scope is a special Python scope that’s created or loaded whenever you run a script. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. 



You can inspect the names and parameters of a function using `.__code__`, which is an attribute that holds information on the function’s internal code. Take a look at the code below:
```python
>>> square.__code__.co_varnames
('base', 'result')
>>> square.__code__.co_argcount
1
>>> square.__code__.co_consts
(None, 2, 'The square of ', ' is: ')
>>> square.__code__.co_name
'square'

```

>If you call dir() without arguments, then you’ll get the list of names that live in your current global scope. Take a look at this code:


you can freely access or reference the value of a global name var within func(). On the other hand, you can’t assign global names inside functions unless you explicitly declare them as global names using a `global` statement. If you try to assign a value to a global name inside a function, then you’ll be creating that name in the function’s local scope


## Modifying the Behavior of a Python Scope

Python provides two keywords that allow you to modify the content of global and nonlocal names. These two keywords are:

1. global
2. nonlocal


#### global 
you can use a global statement. With this statement, you can define a list of names that are going to be treated as global names.


#### nonlocal
With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal. The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas. These names will refer to the same names in the enclosing Python scope.