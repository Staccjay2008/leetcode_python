A phrase is a palindrome if, after converting all uppercase letters into lowercase letters and removing all non-alphanumeric characters, it reads the same forward and backward. Alphanumeric characters include letters and numbers.

Given a string s, return true if it is a palindrome, or false otherwise.

<https://leetcode.com/problems/valid-palindrome/>

#### Approach 1 (python slicing) O(n), O(n)
```python
class Solution:
    def isPalindrome(self, s: str) -> bool:
        if not s:
            return True
        output = []
        for i in s:
            if i.isalnum():
                output.append(i.lower())
        
        return output == output[::-1]
```
#### Approach 2 - two pointer O(n) and O(1)
```python
   class Solution:
    def isPalindrome(self, s: str) -> bool:
        if not s:
            return True
        left, right = 0, len(s)-1
        
        while left < right:
            while left < right and not s[left].isalnum():
                left += 1	
            while left < right and not s[right].isalnum():
                right -= 1

            if left < right and s[left].lower() != s[right].lower():
                return False

            left += 1
            right -= 1
    
        return True
                
