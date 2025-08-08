# Leetcode-2154.-Keep-Multiplying-Found-Values-by-Two
# Description
You are given an array of integers nums. You are also given an integer original which is the first number that needs to be searched for in nums.

You then do the following steps:

If original is found in nums, multiply it by two (i.e., set original = 2 * original).
Otherwise, stop the process.
Repeat this process with the new number as long as you keep finding the number.
Return the final value of original.

# Solution
In the given problem we have been given an array iof integer numbers nums and an original number.

We need to find the original number , if we find the original number in the array nums then multiply it by 2 .

Then keep on repeating this operation till the original number is found in nums.

If the original number is no more found in nums then return the final original number.

# Algorithm
1. Loop through the array nums and check whether originalk number is there or not .
2. If the original number is found then multiply it by 2.
3. Again start from the next number and check whether the newly transformed original number is there in the array.
4. If it is found then again transform the original number by multiplying it by 2 .
5. Return the originak number when it is not to be found.
# Code
class Solution:

    def findFinalValue(self, nums: list[int], original: int) -> int:
        num_set = set(nums)  # Convert list to set for O(1) lookups
        while original in num_set:
            original *= 2
        return original

# Complexity
Time Complexity: O(n)

Converting to set: O(n)

Checking loop: At most O(n) lookups (each O(1)).

Space Complexity: O(n)

Storing elements in a set.
