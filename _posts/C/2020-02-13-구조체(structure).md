---
title: "structure"
layout: post
categories: [C]
tags: [C]
---

- 항상 붙어다녀야 하는 데이터를 별개의 변수들에 분산해서 저장하는 것은 바람직하지 않다.
- 어떤 한 사람의 이름, 전화번호, 이메일 주소 등이 그런 예이다.
- C 언어에서는 이런 경우 구조체(structure)를 사용한다.

- 사용예시

```C
typedef struct person {
	char* name;
	char* number;
	char* email;
	char* group;
}Person;
```

>출처  
><https://www.inflearn.com/course/c%EB%A1%9C-%EB%B0%B0%EC%9A%B0%EB%8A%94-%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0-%EB%B0%8F-%EC%97%AC%EB%9F%AC%EA%B0%80%EC%A7%80-%EC%98%88%EC%A0%9C-%EC%8B%A4%EC%8A%B5/dashboard>
