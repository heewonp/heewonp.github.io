---
layout: post
title: "leetcode 205. Isomorphic Strings(python)"
categories: 코딩테스트
tags: [python,코딩테스트,해시,leetcode]
---


## 문제

Given two strings `s` and `t`, determine if they are isomorphic.

Two strings `s` and `t` are isomorphic if the characters in `s` can be replaced to get `t`.

All occurrences of a character must be replaced with another character while preserving the order of characters. No two characters may map to the same character, but a character may map to itself.


# Example 1:

```
Input: s = "egg", t = "add"
Output: true

```

# Example 2:

```
Input: s = "foo", t = "bar"
Output: false

```
# Example 3:

```
Input: s = "paper", t = "title"
Output: true
```
 

# Constraints:

```
1 <= s.length <= 5 * 104
t.length == s.length
s and t consist of any valid ascii character.

```

## 풀이

```python

class Solution:
    def isIsomorphic(self, s: str, t: str) -> bool:
        
        s_dict ={}
        t_set = set()
        
        for i in range(len(s)):
            if s[i] not in s_dict:
                if t[i] not in t_set:
                
                    s_dict[s[i]] = t[i]
                    t_set.add(t[i])
                    
                else:
                    return False
            else:
                if s_dict[s[i]] != t[i] :
                    
                    return False
        return True


```