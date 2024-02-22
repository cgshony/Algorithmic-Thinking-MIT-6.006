# Algorithmic-Thinking-MIT-6.006
Studies on Algorithms, Data Structures and Python implementation

#---------Binary Search an element----------

def binary_search(arr, x):
    left = 0
    right = len(arr) - 1

    while left <= right:
        mid = (left + right) // 2
        if arr[mid] == x:
            return mid
        elif arr[mid] < x:
            left = mid + 1
        else:
            right = mid -1
    return -1 # if element is not found


arr = [2, 3, 4, 10, 40]
x = 10

result = binary_search(arr, x)

if result != -1:

    print("Element is present at index", str(result))
else:
    print("Element is not present in array")
