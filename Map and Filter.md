# Map and Filter

## Map Function
The map() applies a function to each item in an iterable data

```python
def square(num):
    ''' squares the given num argument '''
    return num ** 2
# end of square

array = list(range(1,11))
square_array = list(map(square, array))
# Original Array: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
# Array Squared: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```
- One thing to note: map() doesn't return any specific data type, just python iterable data
- Therefore, to make it into a list, we have to use the list() function

## Filter Function

`filter(bool_returning_function, sequence)`

- function: The function name we provide for filter() must be return a boolean value ... should also be able handle the items inside the sequence as its arguments
- sequence: any iterable data type

The output of filter will be the input sequence but only with the values that made the function true