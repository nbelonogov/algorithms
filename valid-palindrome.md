# 125. Valid Palindrome

https://leetcode.com/problems/valid-palindrome/

```python
class Solution(object):
    def isPalindrome(self, s):
        clean_string = ''.join([elem for elem in s.lower() if elem.isalnum()])
        head = 0
        tail = len(clean_string) - 1
        while head < tail:
            if clean_string[head] != clean_string[tail]:
                return False
            else:
                head += 1
                tail -= 1
        return True
```