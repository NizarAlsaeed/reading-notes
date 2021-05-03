# In Tests We Trust — TDD with Python

***TDD***: Test-Driven Development is a strategy to think (and write!) tests first.
the idea is to write test at first before the code and then try to pass the tests. 

This way the code will be more reliable andyou will be practicng *software design first*.


# Recursion
The process in which a function calls itself directly or indirectly.

the corresponding function is called as recursive function.

In the recursive program, the solution to the base case is essential as it stops the recursion process.
If the base case is not reached or not defined, then the stack overflow problem may arise

```python

def fact(n):
    if n < = 1:  #<<-----base case
        return 1
    else:    
        return n*fact(n-1)    

```
### direct and indirect recursion
A function fun is called direct recursive if it calls the same function fun. A function fun is called indirect recursive if it calls another function say fun_new and fun_new calls fun directly or indirectly

### disadvantages of recursive programming
less code mqybe but greater space and/or time requirements.

# Python Modules and Packages: An Introduction
Modular programming refers to the process of breaking a large, unwieldy programming task into separate, smaller, more manageable subtasks or modules.

to create a module, just write some code in a file ending with .py and you are done.

to access the module there is options:
- Put .py in the current directory
- Modify the PYTHONPATH environment variable to contain the directory location(that contains the file).
- Put .py in one of the installation-dependent directories (found at 'sys.path').


a try statement with an except ImportError clause can be used to guard against unsuccessful import attempts:
```python
try:
     # Non-existent module
    import baz
except ImportError:
    print('Module not found')
```
