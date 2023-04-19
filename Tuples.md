# Tuples
### What are Tuples?
Tuples are a data type that are:
- immutable
- allow different datatypes as items
- iterable
- nestable (much like a list within a list)

### How to use?
- Declared with empty brackets `()` <-- that's an empty tuple
- `(200,)` is a singleton tuple, comma required so its not seen as an integer
- Sliceable, index using square brackets

### Tuple Operators
**Concatenation**, `a+b`
**Repetition**, `a*3`
**Membership** `a in b`
**Tuples are Iterable, Indexable, and Sliceable**
**Built-in functions** `max, min, len, etc`

### Tuple Comprehension
```python
even_tup = tuple(i for i in range(1,101) if i % 2 == 0)
```

### Tuple & Python: Packing and Unpacking
# Examine the following code
```python
# Packing
var_1 = 2
var_2 = 3
var_3 = 5

prime = var_1, var_2, var_3

print('Packed prime values:', prime)
#Packed prime values: (2, 3, 5)

# Unpacking and Repacking
fib = (0, 1, 1, 2, 3, 5, 8)

fib_0, fib_1, fib_n = fib[0], fib[1], fib[2:]
# fib_0: 0
# fib_1: 1
# fib_n: (1, 2, 3, 5, 8)
```

**Explanation**
- Packing collect multiple variable’s values and assign it to a single variable
- Unpacking help us assign certain values from a tuple to different variables
- This becomes very useful skill when combined with variable arguments for Function Definition and Function Calls