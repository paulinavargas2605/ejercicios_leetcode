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
