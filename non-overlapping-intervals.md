# 435. Non-overlapping Intervals

https://leetcode.com/problems/non-overlapping-intervals/

```python
class Solution(object):
    def eraseOverlapIntervals(self, intervals):
        intervals.sort(key=lambda x: x[0])
        count = 0
        endi = intervals[0][1]
        for i in range(1, len(intervals)):
            if intervals[i][0] < endi:
                count += 1
                endi = min(endi, intervals[i][1])
            else:
                endi = intervals[i][1]
        return count
```