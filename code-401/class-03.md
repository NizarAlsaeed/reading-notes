# Reading and Writing Files in Python (Guide)

to open a file
```python
file = open('path/name.extension)
```
there are two ways that you can use to ensure that a file is closed properly:

1.
```python
#after opening it
try:
    # Further file processing goes here
finally:
    reader.close()
```
2.
```python
#open it using 'with'. It will close automatically
with open('dog_breeds.txt') as reader:
    # Further file processing goes here
```

#### Reading methods
-  `.read(size=2) #based on the number of size bytes`
-   `.readline(size=5) #size number of characters from the line`
-   `.readlines() reads the remaining and returns them as a list.`

```python
# Read and print the entire file line by line
# by looping through .readlines() list 
#OR
# directly from the file:
for line in reader: # reader as defined n method 2
    print(line, end='')
```

> The end='' is to prevent Python from adding an additional newline to the text that is being printed and only print what is being read from the file.

#### Writing methods
-   `.write(string) 	This writes the string to the file.`
-   `.writelines(seq) writes the sequence to the file`
> Appending to a File? use 'a' argument when opening the file.
# Python Exceptions: An Introduction


The try and except block in Python is used to catch and handle exceptions. Python executes code following the try statement as a “normal” part of the program. The code that follows the except statement is the program’s response to any exceptions in the preceding try clause.

#### assert vs try & except:

**assert** *must* be met to continue the execusion. the is no other choice.

**try** can be bypassed by **except** and the program continues execusion.

you can also have**else** and **finally**; else is executed if the try succeed, and finally runs always.

example:

```python
try:
    linux_interaction()
except AssertionError as error:
    print(error)
else:
    try:
        with open('file.log') as file:
            read_data = file.read()
    except FileNotFoundError as fnf_error:
        print(fnf_error)
finally:
    print('Cleaning up, irrespective of any exceptions.')
```
