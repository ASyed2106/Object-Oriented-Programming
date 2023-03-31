# Interable Objects

  → Objects that we can iterate through like a sequence.
    → ex Strings & Lists (sets and dictionaries too)
  → Recall that we could iterate through Strings and Lists
  → To access individual values without indexing, we were able to use for loops
**The portion of the iterable object must be a sequence**

## __iter__() 

  → Allows our object to be iterable, when invoked upon (ex. By a for loop), it will called the method. Commonly just returns it self

## __next__() 
  → Allows us to get to the next value when iterating:

## Common Practice
set an index attribute to -1
increment the index attribute by 1 until self.__index is equal to length of sequence
when the end is reached, raise StopIteration
