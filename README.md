# LeetCode
LeetCode exercises

class Solution:
    def removeDuplicates(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        if len(nums) == 0:
            return 0
        i = 0
        k = 1
        while k < len(nums):
            if nums[i] == nums[k]:
                k +=1
            else:
                i +=1
                nums[i] = nums[k]
                k +=1 
        del nums[i + 1  : len(nums)]
        return i + 1
