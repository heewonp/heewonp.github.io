---
layout: post
title: "leetcode 1.Two Sum"
categories: 코딩테스트
tags: [python,코딩테스트,해시]
---

## 문제
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

Example 1:
```
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
```

Example 2:
````
Input: nums = [3,2,4], target = 6
Output: [1,2]
```

Example 3:
```
Input: nums = [3,3], target = 6
Output: [0,1]
 ```

Constraints:

- `2 <= nums.length <= 104`
- `-109 <= nums[i] <= 109`
- `-109 <= target <= 109`
- Only one valid answer exists.
 


## 풀이

```python


# 풀이 1


# 풀이 2
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        num_dict ={}
        
        for i in range(len(nums)):
            temp = target-nums[i]
            if temp in num_dict:
                return [i,num_dict[temp]]
            num_dict[nums[i]]=i

```
