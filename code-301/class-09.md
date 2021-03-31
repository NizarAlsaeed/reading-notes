# Refactoring


### Concepts of Functional Programming in Javascript

a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data

#### pure functions
1.It returns the same result if given the same arguments
 it should mot use a global object that is not passed as a parameter to the function. 
 The code’s definitely will be easier to test
 
 
 #### Immutability

#### Referential transparency

Basically, if a function consistently yields the same result for the same input, it is referentially transparent.

 We can replace the entire expression with a numerical constant and memoize it.


#### Functions as first-class entities
The idea of functions as first-class entities is that functions are also treated as values and used as data.

#### Reduce

The idea of reduce is to receive a function and a collection, and return a value created by combining the items.

