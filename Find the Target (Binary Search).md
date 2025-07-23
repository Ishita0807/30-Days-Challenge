# Binary Search in a Sorted Array

You are given a sorted array of integers in non-decreasing order and a target value. Your task is to determine the index of the target in the array using binary search.

- If the target exists in the array, print its **0-based index**.  
- If the target does not exist in the array, print **-1**.

---

## Input Format

- First line contains an integer `n` — the size of the array.  
- Second line contains `n` space-separated integers — the elements of the array (sorted in non-decreasing order).  
- Third line contains an integer `target` — the value to search for.

---

## Constraints

- 1 <= n <= 10^5  
- -10^9 <= arr[i], target <= 10^9  
- The array is sorted in non-decreasing order.

---

## Output Format

Print a single integer — the index of `target` in the array, or `-1` if not found.

---

## Sample Input 0
8
-5 -2 0 3 3 3 7 9
3

shell
Copy
Edit

## Sample Output 0
3

yaml
Copy
Edit

---

## Explanation

The value `3` is at index `3`.  
(Any valid index with value `3` is acceptable if multiple occurrences are present.)

---

## Python Code

```python
n = int(input())
arr = list(map(int, input().split()))
target = int(input())

def binarySearch(arr, target):
    low = 0
    high = len(arr) - 1

    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        elif target > arr[mid]:
            low = mid + 1
        else:
            high = mid - 1
    return -1

result = binarySearch(arr, target)
print(result)
