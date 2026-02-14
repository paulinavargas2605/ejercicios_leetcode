# ejercicios_leetcode

class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        """
        complejidad 0(n)
        """
        seen = {}
        
        for i, num in enumerate(nums):
            complemento = target - num
            
            if complemento in seen:
                return [seen[complemento], i]
            
            seen[num] = i

<img width="1857" height="638" alt="twosum" src="https://github.com/user-attachments/assets/7ef00903-4ddd-46a3-bc35-ce8282d139bb" />
