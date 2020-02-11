---
title: "list index"
layout: post
categories: [algorithm]
tags: [algorithm]
---

코드 워즈에서 이런 문제가 나왔다.

Complete the method that takes a boolean value and return a "Yes" string for true, or a "No" string for false.

아래는 내가 제출한 정답

```python
def bool_to_word(boolean):
    if boolean:
        return "Yes"
    else:
        return "No"
```

그런데, 다른 사람들의 코드를 보던 중 신묘한 것을 발견했다.

```python
def bool_to_word(bool):
    return ['No', 'Yes'][bool]
```

어떻게 가능한 걸까?  
파이썬에서, boolean 자료형은 사실 int의 서브클래스라고 한다.  
따라서 'False == 0, True == 1'이 참이 된다.  
이를 이용하여, 위의 코드 ['No', 'Yes'][bool]에서 앞의 ['No', 'Yes'] 부분은 리스트, 뒤의 [bool] 부분은 리스트의 인덱스를 가리키는 것이라고 이해할 수 있다.  
(예) a[10] -> a == 리스트, [10] == 리스트의 인덱스

> 참고링크  
> <https://stackoverflow.com/questions/17742744/python-list-true-false-first-two-elements>
