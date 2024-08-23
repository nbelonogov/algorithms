Написать функцию, которая проверяет правильность строки по всем видам скобок

Examples:
```python
{} - True
[{()(())} - False
[} - False
```
Solution:
```python
def check_brackets(s: str) -> bool:
    stack = []
    brackets = {
        '(': ')',
        '[': ']',
        '{': '}'
    }
    
    for char in s:
        if char in brackets.keys():
            stack.append(char)
        elif char in brackets.values():
            if not stack or brackets[stack.pop()] != char:
                return False
    
    return not stack
```