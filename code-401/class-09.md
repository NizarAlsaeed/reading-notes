# Dunder Methods

a set of predefined methods you can use to enrich your classes.


to unlock the following language features:

- Initialization of new objects > `__init__`
- Object representation > `__str__, __repr__`
- Enable iteration > ` __len__, __getitem__, __reversed__`
```python
def __len__(self):
    return len(self._transactions)

def __getitem__(self, position):
    return self._transactions[position]

def __reversed__(self):
    return self[::-1]

# now you can use 
#1>>> len(acc)
#2>>> for t in acc:
#...    print(t)
#3>>> acc[1]
#4>>> list(reversed(acc))
```
- Operator overloading (comparison) > `__eq__, __lt__`
```python
def __eq__(self, other):
    return self.balance == other.balance

def __lt__(self, other):
    return self.balance < other.balance
```
- Operator overloading (addition) > `__add__`
- Method invocation > `__call__`
- Context manager support (with statement) > `__enter__, __exit__`


# Statistics - Probability
When There are no easy ways to calculate probabilities, so we must fall back on using data and statistics to calculate them.

In probability, the normal distribution is a particular distribution of the probability across all of the events.


### Central Limit Theorem
If we make many estimates, the Central Limit Theorem dictates that the distribution of these estimates will look like a normal distribution.



###  Three Sigma Rule
is an expression of how many of our observations fall within a certain distance of the mean


### The Z-score
is a simple calculation that answers the question, “Given a data point, how many standard deviations is it aw## z-scoreay from the mean?” The equation below is the Z-score equation