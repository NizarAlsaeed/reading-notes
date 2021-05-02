# Pain vs. Suffering

in summary:

pain is what’s necessary to achieve the growth that you’re aiming for.This pain is only temporary.

Suffering is pain without purpose. Pain with no higher goal.



# A beginner's guide to Big O Notation

Big O notation is used in Computer Science to describe the performance or complexity of an algorithm.

Big O specifically describes the **worst-case** scenario.
it can be used to describe:
- the execution time required 

or
- the space used (e.g. in memory or on disk) by an algorithm.

some common orders of growth along with descriptions:

1. O(1)
    >will always execute in the same time (or space) regardless of the size of the input data set.

2. O(N)
    >performance will grow linearly and in direct proportion to the size of the input data set.

3. O(N²)
    >performance is directly proportional to the square of the size of the input data set(nested loops)

4. O(2^N)
    >growth doubles with each addition to the input data set(exponentialy).

5. O(log N)
    >Binary search with iterative halving of data sets which produces a growth curve that peaks at the beginning and slowly flattens out as the size of the data sets increase. *Doubling the size of the input data set has **little** effect on its growth*.
