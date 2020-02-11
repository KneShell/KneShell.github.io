---
title: "gets(), getchar(), isspace()"
layout: post
categories: [C]
tags: [C]
---

- gets(array)

  - 문자열 인자의 길이가 원래의 값을 초과해도 에러 없이 실행한다는 문제가 있다.
  - 대안으로 fgets(array, (int)array_size, stdin)를 사용하길 권장함
  - 이때 stdin은 C언어의 표준입력 파일로써, 키보드로 부터 입력을 받기 위함.
  - fgets는 줄바꿈 문자까지 읽어서 array에 저장

- getchar()

  - 문자를 입력받는 함수
  - 얼핏 보면 char 리턴값이 char 타입일 것 같지만, 실제로는 int 타입이다.

- isspace(char)
  - white space 문자인지 검사하는 함수
  - ctype.h 헤더파일을 필요로함.
