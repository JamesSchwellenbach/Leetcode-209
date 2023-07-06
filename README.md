# Leetcode 209. Minimum Size Subarray Sum (Medium)

#Problem 

Given an array of positive integers nums and a positive integer target, return the minimal length of a 
subarray whose sum is greater than or equal to target. If there is no such subarray, return 0 instead.

Solution - O(n)

Iterate once through the list using two ptrs and a current sum value. Keep track of the leftmost index that is part of the current subbarray and the next value to be added if the subbaray doesn't reach the target sum. if the subarray doesn't add up to the target, add the rightPtr value to the sum and move it to the right one. If it does add up to the target sum, then track if that is the minimum subarray so far and subtract the leftmost value from the sum, adding 1 to leftPtr's index. Keep iterating until rightPtr has reached the end of the list and the sum is insufficent to reach target or if leftPtr reaches the end. Return the smallest subarray size, or 0 if there were no subarrays large enough.
