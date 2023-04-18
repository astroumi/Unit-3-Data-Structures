# Matrices and List Comprehension

## Matrices
- A matrix is basically a 2 dimensional array
- There is matrix data structure, so we use a multiple lists within a list

```python
matrix_A = [
    [1, 2, 3, 4],
    [5, 6, 7, 8]
]

# Accessing Matrix A
print('Row 1: %s' % matrix_A[0]) # Recall: Indexing starts at zero in Python
print('Value at Row 2 Column 2: %s' % matrix_A[1][1])
```

### Rules
- All rows must have the same number of values
- All columns must have the same number of values
- All items in the 2D List must have the same data types
- Since indexing always starts at 0 ... row 1 is technically located at matrix_A[0]

## List Comphrehension
```python
#old way
squares = []
for i in range(10):
    squares.append(i ** 2)

print('Our result: %s' % squares)

#list comprehension
[i**2 for i in range(10)]

#Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```
**Basically:**
- first is the output that each item in the list will have `i**2`
- then is the function that describes the full list (iterable) `for i in range(10)`

### Rules
- A Square Bracket containing an expression that describes the list
- One or more For clause to explain its members
- Then a zero or more if clauses depending on the complexity of the list

```python
a = [1,2,3]
b = [3,1,4]

result = [[x, y] for x in a for y in b if x != y]
#Output: [[1, 3], [1, 4], [2, 3], [2, 1], [2, 4], [3, 1], [3, 4]]
```

Here, each item in the list is another list with x and y. x is from `a` and y is from `b`.