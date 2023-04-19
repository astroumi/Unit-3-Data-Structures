# Dictionaries
Dictionary (Associative Array, map, symbol table) is a data type that stores a collection of (key, value) pairs, such that each possible key appears at most once in the collection.

**Common Operations:**
- Adding a pair
- Removing a pair
- Modify an existing pair
- Lookup of a value associated with a particular key

### Defining Dictionaries
Dictionaries also use {} like sets; however, their individual item format is very different.
Each item in a dictionary be a pair of key: value.
```python
sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
}

# There are 3 items: each with their unique addresses and value
# Accessing
print('Sammy dict:', sammy)
print('Username:', sammy['username'])
```

### Dictionary Properties
**Keys**

Keys are unique address for a dictionary value’s location
- Must be immutable (strings, numbers, tuples, frozenset)
- Unique; therefore, two same key values cannot exist in a single dictionary
  - NEWEST CREATED ITEM with a duplicate KEY superceeds the previous declaration

**Values**

- Values of a dictionary within a key can be any data type.

### Updating a Dictionary
- We can modify existing values by referencing the key
- We can add new values to a dictionary by creating a new key
- We can overwrite a value at an existing key by referencing and recreating the value for it

```python
sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
}

sammy['followers'] += 10 # We are adding 10 to the value located at key: 'followers'
sammy['verified'] = True # We added a new value at a new key: 'verified'
sammy['username'] = 'SammySammy'
```

### Deletion with Dictionary
- We can delete a key hence deleting the value connected to the key `del dict['keyname']`
- We can empty out the entire dictionary `dict.clear()`
- We can delete the dictionary (uncommonly used) `del dict`

```python
sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
}

del sammy['followers'] # del is a keyword used to help us to execute a removal
print('followers key deleted:', sammy)

sammy.clear() # {} is considered an empty dict
print('emptying out a dictionary', sammy)
print('--\n\n')

del sammy
print('Deleting sammy, should create an error when referenced again', sammy)
```

### Membership
Use `in` and `not in` to check membership

```python
sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
}

('username' in sammy) # True
('followers' not in sammy) #False
```

### Built in functions

```python
print('Size of sammy dict:', len(sammy))
print('Largest Key:', max(sammy))
print('Smallest Key:', min(sammy))
print('Dict to string:', str(sammy))
print('Dict to list:', list(sammy))
```

### Duplicate and copy keys only

```python
sammy = {
    'username': 'sammy',
    'online': True,
    'followers': 42
}

sammy_copy1 = sammy.copy()
sammy_copy2 = sammy

sammy['verified'] = True

print('sammy_copy1:', sammy_copy1)
print('sammy_copy2:', sammy_copy2)
print('--')

# Duplicate keys only

tammy = tammy.fromkeys(sammy) # Notice that all key's values are None ... aka empty

print('tammy dict:', tammy)
```

### Dictionary methods

Let A and B be a dictionary

- A.keys() –> Returns a sequence of keys/addresses in A
- A.values() –> Returns a sequence of item values in A
- A.items() –> Returns a sequence of key,item pairs in A
- A.get(address) –> Returns the item value at address
- A.update(B) –> Extends A with the dictionary of key : value pairs of B

### Iterating a dictionary
**We will be taking advantage of three iteration methods**
- iterating the keys
- iterating the values
- iterating the key, value pairs by unpacking

```python
for k, v in sammy.items():
    print('Current Key:', k)
    print('Current Value:', v)
    print()
```

This is an example of unpacking, iterating through something for which each item is also an iterable (in this caase sammy.items returns a tuple with the key and value each time). We can unpack this tuple into two variables (key and value), or `k` and `v`.

### dict() Constrcutor Dictionary Comprehension
We can turn other data types to dictionaries.
Also similar to lists, tuples, and sets, dictionaries also support comprehension.
**Note: We must specify where the keys are and where the values.**

```python
example_data = [
    ('one', 3),
    ('two', 3),
    ('three', 5)
]

data_dict = dict(example_data)
print('data_dict:', data_dict)
print('--')

# Dictionary Comprehension
# Goal: Take string numerals and assign them with their integer square
# - keys : string numerals
# - values: integer squares

example_data2 = ['1', '2', '3', '4', '5']

data2_dict = {x : int(x)**2 for x in example_data2}

print('data2_dict:', data2_dict)
```
**Output:**
`data_dict: {'one': 3, 'two': 3, 'three': 5}`
`--`
`data2_dict: {'1': 1, '2': 4, '3': 9, '4': 16, '5': 25}`
