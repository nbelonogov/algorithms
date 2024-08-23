# 341. Flatten Nested List Iterator

https://leetcode.com/problems/flatten-nested-list-iterator/

```python
class Solution(object):
    def unpacking(nestedlist: list) -> list:
        res = []
        for elem in nestedlist:
            if isinstance(elem, int):
                res.append(elem)
            else:
                res += unpacking(elem)
        return res