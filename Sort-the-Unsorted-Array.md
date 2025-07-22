# Sort the Unsorted Array

You are given an unsorted array of integers. Your task is to sort the array in non-decreasing order and print the sorted array.

---

## Input Format

- The first line contains an integer `n` — the number of elements in the array.  
- The second line contains `n` space-separated integers — the elements of the array.

---

## Constraints

- 1 <= n <= 10^5  
- -10^9 <= arr[i] <= 10^9

---

## Output Format

Print the sorted array in non-decreasing order, with each element separated by a space.

---

## Sample Input 0
5
3 1 4 2 5


## Sample Output 0
1 2 3 4 5


---

## Python Code
```python
n = int(input())
nums = list(map(int, input().split()))
nums.sort()
print(*nums)
