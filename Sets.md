# Sets
### What is a set?
An unordered collection with no duplicate elements in Python 3.
By following the operations and characteristics of the mathematical set, we can utilizie such data structure in our Python code.

- Sets aren’t sliceable nor indexable
- Sets cannot have sets inside them
- Sets do not have order; nor order of insertion
- Sets cannot guarantee that their values will be in order
- Sets do not record a value’s position

### Using Sets in Python
#### How to define a set
```python
example_set1 = {1, 2, 3}
example_set2 = {'h','e','l','l','o'} #removes duplicates
singleton_set = {7}
empty_set = set() # this is because {} is reversed for a different feature in python 3.
```
#### Built in functions
- len
- min
- max
- set(turns iterable into set)

### Operators
- Sets have no duplicates
- **Sets' membership is one of the fastest operations compared to strings, lists, or tuples**
  - We can check whether or not the target exists in our set
- **No indexing in sets because there is no order**
- They are iterable though

### Methods
- Adding values with `exampleSet.add(value)` 
- Removing with `exampleSet.remove(value)` (will give error if not found) or `exampleSet.discard(value)` (won't give error)
- .pop() removes and returns a random value, not recommended
- .clear() empties out the set
  
## Set Operators (math)

### Union
The joining/combining of two sets:
`set1 | set2` or `a.union(b)`
### Intersection
Members/Items that only exists in both sets:
`set1 & set2` or `a.intersection(b)`

### Difference
Members/items that only exists in the first set and not the second set:
`set1 - set2` or `a.difference(b)`
### Symmetric Difference
Members/items that exists one or the other set, but not both sets:
`set1 ^ set2` or `a.symmetric_difference(b)`
### Proper Subset
This is a boolean operator, A is proper subset of B if all members of A are found in B, but A cannot be exactly the same as B:
`Is set1 proper subset of set2?:, set1 < set2` (no method for proper subset)
### Subset
Boolean operator, A is a subset of B if if all members of A are found in B, but A can equal to B unlike a proper subset:
`Is set1 a subset of set2?:, set1 <= set2` or `a.issubset(b)`
### Proper Superset
Boolean operaror, A is a proper superset of B if A has all the values of B and more, but they are not equal to each other:
`Is set1 proper superset of set2?', set1 > set2` (no method for proper superset)
### Superset
Boolean operator, A is a superset of B if A has all the values of B and more, but they can be equal to each other:
`Is set1 superset of set2?:, set1 >= set2` or `a.issuperset(b)`

### Disjoint
Two set are consided disjointed when two sets share no common value.
- Let A and B both represent a set.
- If A & B is empty, then set A and B are considered disjointed.
- To check this in python there is a method called: `a.isdisjoint(b)`

## Updating Methods
```python
# Union and Update --> Update the set, adding elements from all others.
a = set('abracadabra')
b = set('alacazam')

a |= b # same as: a.update(b)
print('Union Update:', a)

# Intersection and Update --> Update the set, keeping only elements found in it and all others.
a = set('abracadabra')
b = set('alacazam')

a &= b # same as: a.intersection_update(b)
print('Intersection Update:', a)

# Difference and Update --> Update the set, removing elements found in others.
a = set('abracadabra')
b = set('alacazam')

a -= b # same as: a.difference_update(b)
print('Difference Update:', a)

# Symmetric Difference and Update --> Update the set, keeping only elements found in either set, but not in both.
a = set('abracadabra')
b = set('alacazam')

a ^= b # same as: a.symmetric_difference_update(b)
print('Symmeteric Difference Update:', a)
```

## Set Comprehension
```python
# Set Comprehension Example
def isPalindrome(x):
    ''' isPalindrome() returns True if string X is a palindrome '''
    return x == x[::-1]

nums = list(range(1,10000))
palindromic_set = {num for num in nums if isPalindrome(str(num))}

print('Palindromic Numbers Set from 1 to 10000:')
print(palindromic_set)
```