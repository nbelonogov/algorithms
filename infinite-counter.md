Write an infinite counter. If a number is passed, it is limited.

```python
def counter(n=None):
    i = 1
    while True:
        if n is not None and i > n:
            break
        yield i
        i += 1
```