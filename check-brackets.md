Write a function that takes a string of parentheses, and determines if the order of the parentheses is valid.
The function should return true if the string is valid, and false if it's invalid.

Examples:
```python
"()"              =>  true
")(()))"          =>  false
"("               =>  false
"(())((()())())"  =>  true
```
Solution:
```python
def valid_parentheses(s: str) -> bool:
    stack = []
    for elem in s:
        if elem == '(':
            stack.append(elem)
        elif elem == ')':
            if not stack:
                return False
            stack.pop()
    return not stack
```