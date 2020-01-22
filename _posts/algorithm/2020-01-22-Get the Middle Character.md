---
title: "Get the Middle Character"
layout: post
categories: [algorithm]
tags: [algorithm]
---
<sub>languege: python</sub>

#### 문제

You are going to be given a word. Your job is to return the middle character of the word. If the word's length is odd, return the middle character. If the word's length is even, return the middle 2 characters.

#### 내가 제출한 코드

```python
def get_middle(s):
    string_length = len(s)

    if string_length % 2 == 0:
        even_index = int(string_length/2)
        return s[even_index - 1] + s[even_index]
    else:
        if string_length == 1:
            return s
        else:
            odd_index = int(string_length/2)
            return s[odd_index]
```

#### 해설

처음에는 문자열을 한 글자씩 쪼개서 리스트로 변환하려했다. 그러나 문자열이 곧 리스트라는 것을 깨닫고, 매개변수로 받은 문자열의 인덱스로 접근하는 방식을 선택했다.
