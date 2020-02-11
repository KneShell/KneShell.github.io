---
title: "strdup, strcpy"
layout: post
categories: [C]
tags: [C]
---

- strdup( string )

  - string duplication
  - 인자로 받은 문자열을 malloc이용해 동적메모리 할당된 임시변수에 복사해 리턴한다.

- strcpy( string1, string2 )
  - string copy
  - 두번째 인자로 받은 문자열을 첫번째 인자에 초기화한다.
  - strdup의 내부에서도 strcpy함수를 사용
