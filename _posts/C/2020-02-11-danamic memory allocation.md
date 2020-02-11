---
title: "동적 메모리 할당 (dynamic memory allocation)"
layout: post
categories: [C]
tags: [C]
---

- 동적 메모리 할당 (dynamic memory allocation)
  - 아무때나 malloc등의 함수를 호출하려 필요한 크기의 메모리를 할당할 수 있다. 이것을 동적 메모리 할당이라고 부른다.
  - 동적으로 할당된 메모리는 힙(heap)이라고 부르는 영역에 위치한다.
  - 동적으로 할당된 메모리는 명시적으로 free()함수를 호출하여 반환하지 않는 한 계속 유지된다.
