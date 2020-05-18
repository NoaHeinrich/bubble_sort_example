# bubble_sort_example
```python
sequence = [4, 3, 5, 0, 1]
# [4, 3, 5, 0, 1]
# [3, 4, 5, 0, 1]
# [3, 4, 5, 0, 1]
# [3, 4, 0, 5, 1]
# [3, 4, 0, 1, 5]


# define bubble_sort that takes an array 
# counter = length of array
# while counter > 0
# iterate through array
#   previous = array[i]
#   current = array[i+1]
#   if previous > current
#       swap previous and current
# counter -= 1

# Your Code Here
def bubble_sort(array):
    swaps = 0
    counter = len(array)
    while counter > 0:
        for index in range(len(array) - 1):
            previous = array[index]
            current = array[index+1]
            if previous > current:
                array[index], array[index+1] = current, previous
                swaps += 1
        counter -= 1
    print(f"Swaps: {swaps}")
    return array

print(f"Final result: {bubble_sort(sequence)}")
```
