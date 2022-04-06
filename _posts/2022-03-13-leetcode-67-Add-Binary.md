---
layout: post
title: "leetcode 67. Add Binary(python)"
categories: 코딩테스트
tags: [python,코딩테스트,leetcode]
---

## 문제

Given two binary strings `a` and `b`, return their sum as a binary string.

 

# Example 1:

```
Input: a = "11", b = "1"
Output: "100"
```

# Example 2:
```
Input: a = "1010", b = "1011"
Output: "10101"
```
 

# Constraints:
```
1 <= a.length, b.length <= 104
a and b consist only of '0' or '1' characters.
Each string does not contain leading zeros except for the zero itself.
```



## 풀이

```python

class Solution:
    def addBinary(self, a: str, b: str) -> str:
        
        return format((int(a,2)+int(b,2)),'b')

```
