---
title: "Sum of positive(8kyu)"
layout: post
categories: [algorithm]
tags: [algorithm]
---
<sub>languege: c#</sub>

#### 문제

You get an array of numbers, return the sum of all of the positives ones.

Example [1,-4,7,12] => 1 + 7 + 12 = 20

Note: if there is nothing to sum, the sum is default to 0.

#### 내가 제출한 코드

```CS
public static int PositiveSum(int[] arr)
  {
    int sum = 0;
    foreach (int item in arr)
    {
       if (item > 0)
       {
          sum += item;
       }
    }
    return sum;
  }
```

#### Best Practices

```CS
public static int PositiveSum(int[] arr)
  {
    return arr.Where(x => x > 0).Sum();
  }
```

 &nbsp;Linq 문법은 마치 무명 메소드 & 람다의 조합처럼 신세계로 느껴진다. 마침 무명 메소드를 배워야겠다는 생각이 들었는데, 이 기회에 한번 찾아봐야겠다.
