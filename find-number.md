Find out if there are two numbers in the ordered list whose sum is equal to target.

Examples:
```python
func([1,2,3,4,5], 6) --> True, тк сумма 2 и 4
func([1,2,3,4,5], 10) --> False, тк нет таких чисел
```
Solution:
```python
def find_pair_sum(numbers, target):
    num_set = set(numbers)
    for num in numbers:
        complement = target - num
        if complement in num_set and complement != num:
            return True
    return False
```