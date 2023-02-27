#### Description
##### Given an array of integers, find two numbers such that they add up to a specific target number.
##### The function twoSum should return indices of the two numbers such that they add up to the target, where index1 must be less than index2. Please note that your returned answers (both index1 and index2) are zero-based.

###### python solution - hashmap
```python
from typing import (
    List,
)

class Solution:
    """
    @param numbers: An array of Integer
    @param target: target = numbers[index1] + numbers[index2]
    @return: [index1, index2] (index1 < index2)
    """
    def two_sum(self, numbers: List[int], target: int) -> List[int]:
        hashmap = {}
        for index, value in enumerate(numbers):
            print(target-value)
            if value in hashmap:   
                return [hashmap[value], index]
            hashmap[target - value] = index
        return [-1,-1]

 # O(n) time, O(n) space   

```

###### python solution - sort + two pointer
```python
from typing import (
    List,
)

class Solution:
    """
    @param numbers: An array of Integer
    @param target: target = numbers[index1] + numbers[index2]
    @return: [index1, index2] (index1 < index2)
    """
    def two_sum(self, numbers: List[int], target: int) -> List[int]:
 

```
